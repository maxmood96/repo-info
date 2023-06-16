<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `flink`

-	[`flink:1.15`](#flink115)
-	[`flink:1.15-java11`](#flink115-java11)
-	[`flink:1.15-java8`](#flink115-java8)
-	[`flink:1.15-scala_2.12`](#flink115-scala_212)
-	[`flink:1.15-scala_2.12-java11`](#flink115-scala_212-java11)
-	[`flink:1.15-scala_2.12-java8`](#flink115-scala_212-java8)
-	[`flink:1.15.4`](#flink1154)
-	[`flink:1.15.4-java11`](#flink1154-java11)
-	[`flink:1.15.4-java8`](#flink1154-java8)
-	[`flink:1.15.4-scala_2.12`](#flink1154-scala_212)
-	[`flink:1.15.4-scala_2.12-java11`](#flink1154-scala_212-java11)
-	[`flink:1.15.4-scala_2.12-java8`](#flink1154-scala_212-java8)
-	[`flink:1.16`](#flink116)
-	[`flink:1.16-java11`](#flink116-java11)
-	[`flink:1.16-java8`](#flink116-java8)
-	[`flink:1.16-scala_2.12`](#flink116-scala_212)
-	[`flink:1.16-scala_2.12-java11`](#flink116-scala_212-java11)
-	[`flink:1.16-scala_2.12-java8`](#flink116-scala_212-java8)
-	[`flink:1.16.2`](#flink1162)
-	[`flink:1.16.2-java11`](#flink1162-java11)
-	[`flink:1.16.2-java8`](#flink1162-java8)
-	[`flink:1.16.2-scala_2.12`](#flink1162-scala_212)
-	[`flink:1.16.2-scala_2.12-java11`](#flink1162-scala_212-java11)
-	[`flink:1.16.2-scala_2.12-java8`](#flink1162-scala_212-java8)
-	[`flink:1.17`](#flink117)
-	[`flink:1.17-java11`](#flink117-java11)
-	[`flink:1.17-java8`](#flink117-java8)
-	[`flink:1.17-scala_2.12`](#flink117-scala_212)
-	[`flink:1.17-scala_2.12-java11`](#flink117-scala_212-java11)
-	[`flink:1.17-scala_2.12-java8`](#flink117-scala_212-java8)
-	[`flink:1.17.1`](#flink1171)
-	[`flink:1.17.1-java11`](#flink1171-java11)
-	[`flink:1.17.1-java8`](#flink1171-java8)
-	[`flink:1.17.1-scala_2.12`](#flink1171-scala_212)
-	[`flink:1.17.1-scala_2.12-java11`](#flink1171-scala_212-java11)
-	[`flink:1.17.1-scala_2.12-java8`](#flink1171-scala_212-java8)
-	[`flink:java11`](#flinkjava11)
-	[`flink:java8`](#flinkjava8)
-	[`flink:latest`](#flinklatest)
-	[`flink:scala_2.12`](#flinkscala_212)
-	[`flink:scala_2.12-java11`](#flinkscala_212-java11)
-	[`flink:scala_2.12-java8`](#flinkscala_212-java8)

## `flink:1.15`

```console
$ docker pull flink@sha256:7c861deb8057815d60a6ff8b8eeb8bdc9535c90cd05bbf27f74e412b906a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15` - linux; amd64

```console
$ docker pull flink@sha256:1797e201d203471f532622ebdae5466ab58a631662646b4899b6c65104347d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf4b01a6e517034314083880ba6721c4065fec212e7e3a22526d892129ade3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:46 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:47 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:42:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:42:19 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:42:19 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:42:19 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a5bde52d0b61226459a7d6c9ebf9d649b9bbec4704fd707aaafb9ac30a208`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9fd72d2b65dccd13e6f8879a61b11aa41ff2ce48a5f32ec4442b09d2d0ca2`  
		Last Modified: Fri, 16 Jun 2023 07:45:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8135b654360f4a86b656ca9b702a44eb6a1a3644697d30da7b496a7df98484a`  
		Last Modified: Fri, 16 Jun 2023 07:46:09 GMT  
		Size: 436.3 MB (436280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17119fe5e3eee5209129d966f3d9295395e4670705c2d15d713607ac26f2d629`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f0b3fbb581e6fe318228f8ad83392fdeee3c622a2a5618efdb0c30ce2bdf442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527478893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb93123b964b087bc2752ec391db3fa1ee8e9c3e2e38dcbb06e22555d3a2258`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:49 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:34:06 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:34:09 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:34:09 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:34:09 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe325eaeec21e6ee96cb43cf53bd191acc4413f3ac3f4b630dd57a3b7d1c769`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8695132e1b7a8e7a78aae5f841317d591d103baa6e659de4dd7a181a402fb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b31d89184297ce3adf9d51aaabe0a5ef7f32b0898ddc5571e1494d08439dae`  
		Last Modified: Fri, 16 Jun 2023 04:37:37 GMT  
		Size: 436.3 MB (436280045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e0db28fc9244f8fab1be5a4e3b51e068774b0a562fe304cd1997b297209cb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-java11`

```console
$ docker pull flink@sha256:7c861deb8057815d60a6ff8b8eeb8bdc9535c90cd05bbf27f74e412b906a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-java11` - linux; amd64

```console
$ docker pull flink@sha256:1797e201d203471f532622ebdae5466ab58a631662646b4899b6c65104347d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf4b01a6e517034314083880ba6721c4065fec212e7e3a22526d892129ade3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:46 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:47 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:42:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:42:19 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:42:19 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:42:19 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a5bde52d0b61226459a7d6c9ebf9d649b9bbec4704fd707aaafb9ac30a208`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9fd72d2b65dccd13e6f8879a61b11aa41ff2ce48a5f32ec4442b09d2d0ca2`  
		Last Modified: Fri, 16 Jun 2023 07:45:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8135b654360f4a86b656ca9b702a44eb6a1a3644697d30da7b496a7df98484a`  
		Last Modified: Fri, 16 Jun 2023 07:46:09 GMT  
		Size: 436.3 MB (436280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17119fe5e3eee5209129d966f3d9295395e4670705c2d15d713607ac26f2d629`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f0b3fbb581e6fe318228f8ad83392fdeee3c622a2a5618efdb0c30ce2bdf442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527478893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb93123b964b087bc2752ec391db3fa1ee8e9c3e2e38dcbb06e22555d3a2258`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:49 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:34:06 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:34:09 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:34:09 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:34:09 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe325eaeec21e6ee96cb43cf53bd191acc4413f3ac3f4b630dd57a3b7d1c769`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8695132e1b7a8e7a78aae5f841317d591d103baa6e659de4dd7a181a402fb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b31d89184297ce3adf9d51aaabe0a5ef7f32b0898ddc5571e1494d08439dae`  
		Last Modified: Fri, 16 Jun 2023 04:37:37 GMT  
		Size: 436.3 MB (436280045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e0db28fc9244f8fab1be5a4e3b51e068774b0a562fe304cd1997b297209cb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-java8`

```console
$ docker pull flink@sha256:1308770a95ecacf23ee53637c14cda073daec225db722c5f8acfa06930ab1b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-java8` - linux; amd64

```console
$ docker pull flink@sha256:6643eabeae696b8fb45ab2ce88616397ff61a397957d23ee3d0c60ac71ab21c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.6 MB (526604610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c15508903920297798f601e17cd896fd251215705212884ac53be9bab96a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:05 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:05 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:05 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:06 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:06 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:41:38 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:41:39 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:41:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:41:40 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:41:40 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cb232d470e8b506e696eef3745c74aced027cdf9c519782091def4ba141c3`  
		Last Modified: Fri, 16 Jun 2023 07:45:22 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6268fb8b85eaa97acf33b0a0a2b94410d88de0ff0b6631270ad12500266051d7`  
		Last Modified: Fri, 16 Jun 2023 07:45:21 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935dfcbbbe6ed56b8329f32b355018af8c3fe651a83149c86bd496c3ac9afbdb`  
		Last Modified: Fri, 16 Jun 2023 07:45:39 GMT  
		Size: 436.3 MB (436280099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b38b62ea7a77edc2dc804d506523c3a43fba0337ab31e2633c9ded20349d987`  
		Last Modified: Fri, 16 Jun 2023 07:45:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:20a333dc578fa957b866cb4d5bfe7a524dac717f4c7712eb04dd0ea754eb1fb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523290481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a479f69d36cfaa0af7c728c6eeea667246a93132ec359d074d33661ec73b386`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:01 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:01 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:01 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:01 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:33:38 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:33:40 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:33:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:33:41 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:33:41 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa5f7625a5d62b2e254baac7dace247e2bf8114b94c6349cb549390063313db`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 4.7 KB (4652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0277b41361cd14eef92b24559d6c9f5794d830ea37ad70db30855f62cc544c`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531d8e774066b0b74c243578674647fc8748d1c529fb4243d6cf69b02612051`  
		Last Modified: Fri, 16 Jun 2023 04:37:10 GMT  
		Size: 436.3 MB (436280031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18531d0392d8be9f97e6594372978605257e2daee5a2b178210e771b7e94a652`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-scala_2.12`

```console
$ docker pull flink@sha256:7c861deb8057815d60a6ff8b8eeb8bdc9535c90cd05bbf27f74e412b906a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:1797e201d203471f532622ebdae5466ab58a631662646b4899b6c65104347d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf4b01a6e517034314083880ba6721c4065fec212e7e3a22526d892129ade3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:46 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:47 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:42:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:42:19 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:42:19 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:42:19 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a5bde52d0b61226459a7d6c9ebf9d649b9bbec4704fd707aaafb9ac30a208`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9fd72d2b65dccd13e6f8879a61b11aa41ff2ce48a5f32ec4442b09d2d0ca2`  
		Last Modified: Fri, 16 Jun 2023 07:45:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8135b654360f4a86b656ca9b702a44eb6a1a3644697d30da7b496a7df98484a`  
		Last Modified: Fri, 16 Jun 2023 07:46:09 GMT  
		Size: 436.3 MB (436280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17119fe5e3eee5209129d966f3d9295395e4670705c2d15d713607ac26f2d629`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f0b3fbb581e6fe318228f8ad83392fdeee3c622a2a5618efdb0c30ce2bdf442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527478893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb93123b964b087bc2752ec391db3fa1ee8e9c3e2e38dcbb06e22555d3a2258`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:49 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:34:06 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:34:09 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:34:09 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:34:09 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe325eaeec21e6ee96cb43cf53bd191acc4413f3ac3f4b630dd57a3b7d1c769`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8695132e1b7a8e7a78aae5f841317d591d103baa6e659de4dd7a181a402fb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b31d89184297ce3adf9d51aaabe0a5ef7f32b0898ddc5571e1494d08439dae`  
		Last Modified: Fri, 16 Jun 2023 04:37:37 GMT  
		Size: 436.3 MB (436280045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e0db28fc9244f8fab1be5a4e3b51e068774b0a562fe304cd1997b297209cb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-scala_2.12-java11`

```console
$ docker pull flink@sha256:7c861deb8057815d60a6ff8b8eeb8bdc9535c90cd05bbf27f74e412b906a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:1797e201d203471f532622ebdae5466ab58a631662646b4899b6c65104347d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf4b01a6e517034314083880ba6721c4065fec212e7e3a22526d892129ade3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:46 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:47 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:42:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:42:19 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:42:19 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:42:19 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a5bde52d0b61226459a7d6c9ebf9d649b9bbec4704fd707aaafb9ac30a208`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9fd72d2b65dccd13e6f8879a61b11aa41ff2ce48a5f32ec4442b09d2d0ca2`  
		Last Modified: Fri, 16 Jun 2023 07:45:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8135b654360f4a86b656ca9b702a44eb6a1a3644697d30da7b496a7df98484a`  
		Last Modified: Fri, 16 Jun 2023 07:46:09 GMT  
		Size: 436.3 MB (436280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17119fe5e3eee5209129d966f3d9295395e4670705c2d15d713607ac26f2d629`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f0b3fbb581e6fe318228f8ad83392fdeee3c622a2a5618efdb0c30ce2bdf442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527478893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb93123b964b087bc2752ec391db3fa1ee8e9c3e2e38dcbb06e22555d3a2258`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:49 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:34:06 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:34:09 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:34:09 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:34:09 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe325eaeec21e6ee96cb43cf53bd191acc4413f3ac3f4b630dd57a3b7d1c769`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8695132e1b7a8e7a78aae5f841317d591d103baa6e659de4dd7a181a402fb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b31d89184297ce3adf9d51aaabe0a5ef7f32b0898ddc5571e1494d08439dae`  
		Last Modified: Fri, 16 Jun 2023 04:37:37 GMT  
		Size: 436.3 MB (436280045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e0db28fc9244f8fab1be5a4e3b51e068774b0a562fe304cd1997b297209cb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15-scala_2.12-java8`

```console
$ docker pull flink@sha256:1308770a95ecacf23ee53637c14cda073daec225db722c5f8acfa06930ab1b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:6643eabeae696b8fb45ab2ce88616397ff61a397957d23ee3d0c60ac71ab21c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.6 MB (526604610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c15508903920297798f601e17cd896fd251215705212884ac53be9bab96a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:05 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:05 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:05 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:06 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:06 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:41:38 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:41:39 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:41:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:41:40 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:41:40 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cb232d470e8b506e696eef3745c74aced027cdf9c519782091def4ba141c3`  
		Last Modified: Fri, 16 Jun 2023 07:45:22 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6268fb8b85eaa97acf33b0a0a2b94410d88de0ff0b6631270ad12500266051d7`  
		Last Modified: Fri, 16 Jun 2023 07:45:21 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935dfcbbbe6ed56b8329f32b355018af8c3fe651a83149c86bd496c3ac9afbdb`  
		Last Modified: Fri, 16 Jun 2023 07:45:39 GMT  
		Size: 436.3 MB (436280099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b38b62ea7a77edc2dc804d506523c3a43fba0337ab31e2633c9ded20349d987`  
		Last Modified: Fri, 16 Jun 2023 07:45:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:20a333dc578fa957b866cb4d5bfe7a524dac717f4c7712eb04dd0ea754eb1fb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523290481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a479f69d36cfaa0af7c728c6eeea667246a93132ec359d074d33661ec73b386`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:01 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:01 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:01 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:01 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:33:38 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:33:40 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:33:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:33:41 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:33:41 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa5f7625a5d62b2e254baac7dace247e2bf8114b94c6349cb549390063313db`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 4.7 KB (4652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0277b41361cd14eef92b24559d6c9f5794d830ea37ad70db30855f62cc544c`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531d8e774066b0b74c243578674647fc8748d1c529fb4243d6cf69b02612051`  
		Last Modified: Fri, 16 Jun 2023 04:37:10 GMT  
		Size: 436.3 MB (436280031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18531d0392d8be9f97e6594372978605257e2daee5a2b178210e771b7e94a652`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.4`

```console
$ docker pull flink@sha256:7c861deb8057815d60a6ff8b8eeb8bdc9535c90cd05bbf27f74e412b906a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.4` - linux; amd64

```console
$ docker pull flink@sha256:1797e201d203471f532622ebdae5466ab58a631662646b4899b6c65104347d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf4b01a6e517034314083880ba6721c4065fec212e7e3a22526d892129ade3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:46 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:47 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:42:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:42:19 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:42:19 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:42:19 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a5bde52d0b61226459a7d6c9ebf9d649b9bbec4704fd707aaafb9ac30a208`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9fd72d2b65dccd13e6f8879a61b11aa41ff2ce48a5f32ec4442b09d2d0ca2`  
		Last Modified: Fri, 16 Jun 2023 07:45:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8135b654360f4a86b656ca9b702a44eb6a1a3644697d30da7b496a7df98484a`  
		Last Modified: Fri, 16 Jun 2023 07:46:09 GMT  
		Size: 436.3 MB (436280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17119fe5e3eee5209129d966f3d9295395e4670705c2d15d713607ac26f2d629`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.4` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f0b3fbb581e6fe318228f8ad83392fdeee3c622a2a5618efdb0c30ce2bdf442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527478893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb93123b964b087bc2752ec391db3fa1ee8e9c3e2e38dcbb06e22555d3a2258`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:49 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:34:06 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:34:09 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:34:09 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:34:09 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe325eaeec21e6ee96cb43cf53bd191acc4413f3ac3f4b630dd57a3b7d1c769`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8695132e1b7a8e7a78aae5f841317d591d103baa6e659de4dd7a181a402fb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b31d89184297ce3adf9d51aaabe0a5ef7f32b0898ddc5571e1494d08439dae`  
		Last Modified: Fri, 16 Jun 2023 04:37:37 GMT  
		Size: 436.3 MB (436280045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e0db28fc9244f8fab1be5a4e3b51e068774b0a562fe304cd1997b297209cb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.4-java11`

```console
$ docker pull flink@sha256:7c861deb8057815d60a6ff8b8eeb8bdc9535c90cd05bbf27f74e412b906a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.4-java11` - linux; amd64

```console
$ docker pull flink@sha256:1797e201d203471f532622ebdae5466ab58a631662646b4899b6c65104347d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf4b01a6e517034314083880ba6721c4065fec212e7e3a22526d892129ade3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:46 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:47 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:42:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:42:19 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:42:19 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:42:19 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a5bde52d0b61226459a7d6c9ebf9d649b9bbec4704fd707aaafb9ac30a208`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9fd72d2b65dccd13e6f8879a61b11aa41ff2ce48a5f32ec4442b09d2d0ca2`  
		Last Modified: Fri, 16 Jun 2023 07:45:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8135b654360f4a86b656ca9b702a44eb6a1a3644697d30da7b496a7df98484a`  
		Last Modified: Fri, 16 Jun 2023 07:46:09 GMT  
		Size: 436.3 MB (436280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17119fe5e3eee5209129d966f3d9295395e4670705c2d15d713607ac26f2d629`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.4-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f0b3fbb581e6fe318228f8ad83392fdeee3c622a2a5618efdb0c30ce2bdf442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527478893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb93123b964b087bc2752ec391db3fa1ee8e9c3e2e38dcbb06e22555d3a2258`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:49 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:34:06 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:34:09 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:34:09 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:34:09 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe325eaeec21e6ee96cb43cf53bd191acc4413f3ac3f4b630dd57a3b7d1c769`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8695132e1b7a8e7a78aae5f841317d591d103baa6e659de4dd7a181a402fb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b31d89184297ce3adf9d51aaabe0a5ef7f32b0898ddc5571e1494d08439dae`  
		Last Modified: Fri, 16 Jun 2023 04:37:37 GMT  
		Size: 436.3 MB (436280045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e0db28fc9244f8fab1be5a4e3b51e068774b0a562fe304cd1997b297209cb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.4-java8`

```console
$ docker pull flink@sha256:1308770a95ecacf23ee53637c14cda073daec225db722c5f8acfa06930ab1b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.4-java8` - linux; amd64

```console
$ docker pull flink@sha256:6643eabeae696b8fb45ab2ce88616397ff61a397957d23ee3d0c60ac71ab21c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.6 MB (526604610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c15508903920297798f601e17cd896fd251215705212884ac53be9bab96a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:05 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:05 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:05 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:06 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:06 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:41:38 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:41:39 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:41:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:41:40 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:41:40 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cb232d470e8b506e696eef3745c74aced027cdf9c519782091def4ba141c3`  
		Last Modified: Fri, 16 Jun 2023 07:45:22 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6268fb8b85eaa97acf33b0a0a2b94410d88de0ff0b6631270ad12500266051d7`  
		Last Modified: Fri, 16 Jun 2023 07:45:21 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935dfcbbbe6ed56b8329f32b355018af8c3fe651a83149c86bd496c3ac9afbdb`  
		Last Modified: Fri, 16 Jun 2023 07:45:39 GMT  
		Size: 436.3 MB (436280099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b38b62ea7a77edc2dc804d506523c3a43fba0337ab31e2633c9ded20349d987`  
		Last Modified: Fri, 16 Jun 2023 07:45:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.4-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:20a333dc578fa957b866cb4d5bfe7a524dac717f4c7712eb04dd0ea754eb1fb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523290481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a479f69d36cfaa0af7c728c6eeea667246a93132ec359d074d33661ec73b386`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:01 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:01 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:01 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:01 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:33:38 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:33:40 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:33:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:33:41 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:33:41 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa5f7625a5d62b2e254baac7dace247e2bf8114b94c6349cb549390063313db`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 4.7 KB (4652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0277b41361cd14eef92b24559d6c9f5794d830ea37ad70db30855f62cc544c`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531d8e774066b0b74c243578674647fc8748d1c529fb4243d6cf69b02612051`  
		Last Modified: Fri, 16 Jun 2023 04:37:10 GMT  
		Size: 436.3 MB (436280031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18531d0392d8be9f97e6594372978605257e2daee5a2b178210e771b7e94a652`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.4-scala_2.12`

```console
$ docker pull flink@sha256:7c861deb8057815d60a6ff8b8eeb8bdc9535c90cd05bbf27f74e412b906a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.4-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:1797e201d203471f532622ebdae5466ab58a631662646b4899b6c65104347d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf4b01a6e517034314083880ba6721c4065fec212e7e3a22526d892129ade3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:46 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:47 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:42:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:42:19 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:42:19 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:42:19 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a5bde52d0b61226459a7d6c9ebf9d649b9bbec4704fd707aaafb9ac30a208`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9fd72d2b65dccd13e6f8879a61b11aa41ff2ce48a5f32ec4442b09d2d0ca2`  
		Last Modified: Fri, 16 Jun 2023 07:45:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8135b654360f4a86b656ca9b702a44eb6a1a3644697d30da7b496a7df98484a`  
		Last Modified: Fri, 16 Jun 2023 07:46:09 GMT  
		Size: 436.3 MB (436280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17119fe5e3eee5209129d966f3d9295395e4670705c2d15d713607ac26f2d629`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.4-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f0b3fbb581e6fe318228f8ad83392fdeee3c622a2a5618efdb0c30ce2bdf442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527478893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb93123b964b087bc2752ec391db3fa1ee8e9c3e2e38dcbb06e22555d3a2258`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:49 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:34:06 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:34:09 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:34:09 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:34:09 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe325eaeec21e6ee96cb43cf53bd191acc4413f3ac3f4b630dd57a3b7d1c769`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8695132e1b7a8e7a78aae5f841317d591d103baa6e659de4dd7a181a402fb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b31d89184297ce3adf9d51aaabe0a5ef7f32b0898ddc5571e1494d08439dae`  
		Last Modified: Fri, 16 Jun 2023 04:37:37 GMT  
		Size: 436.3 MB (436280045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e0db28fc9244f8fab1be5a4e3b51e068774b0a562fe304cd1997b297209cb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.4-scala_2.12-java11`

```console
$ docker pull flink@sha256:7c861deb8057815d60a6ff8b8eeb8bdc9535c90cd05bbf27f74e412b906a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.4-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:1797e201d203471f532622ebdae5466ab58a631662646b4899b6c65104347d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf4b01a6e517034314083880ba6721c4065fec212e7e3a22526d892129ade3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:46 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:46 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:47 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:42:18 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:42:19 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:42:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:42:19 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:42:19 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a5bde52d0b61226459a7d6c9ebf9d649b9bbec4704fd707aaafb9ac30a208`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d9fd72d2b65dccd13e6f8879a61b11aa41ff2ce48a5f32ec4442b09d2d0ca2`  
		Last Modified: Fri, 16 Jun 2023 07:45:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8135b654360f4a86b656ca9b702a44eb6a1a3644697d30da7b496a7df98484a`  
		Last Modified: Fri, 16 Jun 2023 07:46:09 GMT  
		Size: 436.3 MB (436280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17119fe5e3eee5209129d966f3d9295395e4670705c2d15d713607ac26f2d629`  
		Last Modified: Fri, 16 Jun 2023 07:45:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.4-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:f0b3fbb581e6fe318228f8ad83392fdeee3c622a2a5618efdb0c30ce2bdf442c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527478893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb93123b964b087bc2752ec391db3fa1ee8e9c3e2e38dcbb06e22555d3a2258`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:49 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:49 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:49 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:49 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:34:06 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:34:09 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:34:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:34:09 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:34:09 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe325eaeec21e6ee96cb43cf53bd191acc4413f3ac3f4b630dd57a3b7d1c769`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 4.6 KB (4648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8695132e1b7a8e7a78aae5f841317d591d103baa6e659de4dd7a181a402fb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b31d89184297ce3adf9d51aaabe0a5ef7f32b0898ddc5571e1494d08439dae`  
		Last Modified: Fri, 16 Jun 2023 04:37:37 GMT  
		Size: 436.3 MB (436280045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e0db28fc9244f8fab1be5a4e3b51e068774b0a562fe304cd1997b297209cb`  
		Last Modified: Fri, 16 Jun 2023 04:37:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.15.4-scala_2.12-java8`

```console
$ docker pull flink@sha256:1308770a95ecacf23ee53637c14cda073daec225db722c5f8acfa06930ab1b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.15.4-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:6643eabeae696b8fb45ab2ce88616397ff61a397957d23ee3d0c60ac71ab21c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.6 MB (526604610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c15508903920297798f601e17cd896fd251215705212884ac53be9bab96a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:41:05 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 07:41:05 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:41:05 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:41:06 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:41:06 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:41:38 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:41:39 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:41:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:41:40 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:41:40 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cb232d470e8b506e696eef3745c74aced027cdf9c519782091def4ba141c3`  
		Last Modified: Fri, 16 Jun 2023 07:45:22 GMT  
		Size: 4.6 KB (4609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6268fb8b85eaa97acf33b0a0a2b94410d88de0ff0b6631270ad12500266051d7`  
		Last Modified: Fri, 16 Jun 2023 07:45:21 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935dfcbbbe6ed56b8329f32b355018af8c3fe651a83149c86bd496c3ac9afbdb`  
		Last Modified: Fri, 16 Jun 2023 07:45:39 GMT  
		Size: 436.3 MB (436280099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b38b62ea7a77edc2dc804d506523c3a43fba0337ab31e2633c9ded20349d987`  
		Last Modified: Fri, 16 Jun 2023 07:45:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.15.4-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:20a333dc578fa957b866cb4d5bfe7a524dac717f4c7712eb04dd0ea754eb1fb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523290481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a479f69d36cfaa0af7c728c6eeea667246a93132ec359d074d33661ec73b386`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:33:01 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.4/flink-1.15.4-bin-scala_2.12.tgz.asc GPG_KEY=0F79F2AFB2351BC29678544591F9C1EC125FD8DB CHECK_GPG=true
# Fri, 16 Jun 2023 04:33:01 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:33:01 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:33:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:33:01 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:33:38 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:33:40 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:33:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:33:41 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:33:41 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa5f7625a5d62b2e254baac7dace247e2bf8114b94c6349cb549390063313db`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 4.7 KB (4652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0277b41361cd14eef92b24559d6c9f5794d830ea37ad70db30855f62cc544c`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d531d8e774066b0b74c243578674647fc8748d1c529fb4243d6cf69b02612051`  
		Last Modified: Fri, 16 Jun 2023 04:37:10 GMT  
		Size: 436.3 MB (436280031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18531d0392d8be9f97e6594372978605257e2daee5a2b178210e771b7e94a652`  
		Last Modified: Fri, 16 Jun 2023 04:36:54 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16`

```console
$ docker pull flink@sha256:34e8e2990ee21b27854e50e24e4bfeeda473d2e580054b9c884e4f488c6b3557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16` - linux; amd64

```console
$ docker pull flink@sha256:59394226f0392d43c8621eef0c4a1f82bfc57ce54b1947e50298ca009e30558c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569873610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f030983e366e8027e68675cf6aaeaf8ca2d5b0125fd5fab1bef93ca834dea6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:40:07 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:40:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:40:07 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:40:55 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:40:56 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:40:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:40:57 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:40:57 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fb05d6c9821a7ff3202d9e895fb6991a0fa4c38ef84cdbc4591b3445cd648`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84280fff4fea28aa843e6a641415aab2d3928e6aaf87af8d67821bab8025f36`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159665277aa747535ac0cff9e0dc6314c4c383a85ee04b2d1f17818654b63c`  
		Last Modified: Fri, 16 Jun 2023 07:44:59 GMT  
		Size: 474.7 MB (474720057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89a67fa322a3e521fc8dc5c99232a7a41e02e13a6c47ae4d7985d399d66a998`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e24e99cfadeef9f01a724dc3755ec15aa3e858d15148a23a3568a66e1c4bb92e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565918872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaa0b3ec6bb44464adfcddd9edbd344d7bcf7fad111b6d553c0ea09176ed08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:32:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:32:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:32:33 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:51 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:54 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:54 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792070497b5a1fcfaf1913ff3d564f760d3d96a745fc1ef620012f7a0a555b6`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d772ec46d67513a5e4aebe575fab628faacaa0166947e648bb0446599807a`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4e455d43050e6bd09f037fd4fc6816b68d47e7b4ba7c1424fb88000e99a124`  
		Last Modified: Fri, 16 Jun 2023 04:36:34 GMT  
		Size: 474.7 MB (474720017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e760faff74565c71228c73ddf609bfee9f5691119c4f10525f03562956d3fc1`  
		Last Modified: Fri, 16 Jun 2023 04:36:19 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-java11`

```console
$ docker pull flink@sha256:34e8e2990ee21b27854e50e24e4bfeeda473d2e580054b9c884e4f488c6b3557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-java11` - linux; amd64

```console
$ docker pull flink@sha256:59394226f0392d43c8621eef0c4a1f82bfc57ce54b1947e50298ca009e30558c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569873610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f030983e366e8027e68675cf6aaeaf8ca2d5b0125fd5fab1bef93ca834dea6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:40:07 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:40:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:40:07 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:40:55 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:40:56 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:40:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:40:57 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:40:57 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fb05d6c9821a7ff3202d9e895fb6991a0fa4c38ef84cdbc4591b3445cd648`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84280fff4fea28aa843e6a641415aab2d3928e6aaf87af8d67821bab8025f36`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159665277aa747535ac0cff9e0dc6314c4c383a85ee04b2d1f17818654b63c`  
		Last Modified: Fri, 16 Jun 2023 07:44:59 GMT  
		Size: 474.7 MB (474720057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89a67fa322a3e521fc8dc5c99232a7a41e02e13a6c47ae4d7985d399d66a998`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e24e99cfadeef9f01a724dc3755ec15aa3e858d15148a23a3568a66e1c4bb92e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565918872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaa0b3ec6bb44464adfcddd9edbd344d7bcf7fad111b6d553c0ea09176ed08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:32:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:32:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:32:33 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:51 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:54 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:54 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792070497b5a1fcfaf1913ff3d564f760d3d96a745fc1ef620012f7a0a555b6`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d772ec46d67513a5e4aebe575fab628faacaa0166947e648bb0446599807a`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4e455d43050e6bd09f037fd4fc6816b68d47e7b4ba7c1424fb88000e99a124`  
		Last Modified: Fri, 16 Jun 2023 04:36:34 GMT  
		Size: 474.7 MB (474720017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e760faff74565c71228c73ddf609bfee9f5691119c4f10525f03562956d3fc1`  
		Last Modified: Fri, 16 Jun 2023 04:36:19 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-java8`

```console
$ docker pull flink@sha256:7acc4a846999e1c6b0e7c8e9b39cf7a2c623b466bc3002d16443056d12ece0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-java8` - linux; amd64

```console
$ docker pull flink@sha256:15e6fc6c8be28040da94f0daaefc0b3395faafa9e454a9ec528fa79bec023bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.0 MB (565044644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e23e69aea0c29721a2b7568615c7000b0b8affd06fa051274a24aeee3e66f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:39:25 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:39:26 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:39:26 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:39:26 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:39:26 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:58 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:58 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:58 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38988a938e7c26e5210e4ec3ffa60e16a62af570cbc5e92efb36afa2beef7539`  
		Last Modified: Fri, 16 Jun 2023 07:44:08 GMT  
		Size: 4.6 KB (4611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01fbbf7a7ec70fdc13dded3e45e158e0ccc31430f5e1a74e3c808ee6b0238ce`  
		Last Modified: Fri, 16 Jun 2023 07:44:09 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cb21082895019bba7b17bfa447f37da20a66fa83a6b33f00ab9371a1f62275`  
		Last Modified: Fri, 16 Jun 2023 07:44:28 GMT  
		Size: 474.7 MB (474720129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46106bb814865f3b9804933650885edf1c7b1950442a0403954e3c3ae8eaa5f`  
		Last Modified: Fri, 16 Jun 2023 07:44:09 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:b4542098079bcb108d4c01403b764df4e9f913d0d77e92521ae2ba290df842d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561730485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5b4d10b10af0fc537cd5b917add9b25fe9e097afea6f5e26413d17393826d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:45 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:45 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:45 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:45 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:45 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:27 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:30 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:30 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:30 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bf50c5781afffe889f5f00aec6ccb6e9472e4604bb156b3e27363040130d4`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff268c2a1badc9a52a1501cbb84aa76b4847aa5a5721dfd1682a60a2da7ef515`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f4c5b5ed54a1c4720d5a2748758c8e235fd6ca5c3927ea3882bc1c59871572`  
		Last Modified: Fri, 16 Jun 2023 04:36:06 GMT  
		Size: 474.7 MB (474720039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45714402c098a84e9ed4c71a16e96dfa895f58ab4d9ab0d848652b4f567cf4e`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-scala_2.12`

```console
$ docker pull flink@sha256:34e8e2990ee21b27854e50e24e4bfeeda473d2e580054b9c884e4f488c6b3557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:59394226f0392d43c8621eef0c4a1f82bfc57ce54b1947e50298ca009e30558c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569873610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f030983e366e8027e68675cf6aaeaf8ca2d5b0125fd5fab1bef93ca834dea6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:40:07 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:40:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:40:07 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:40:55 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:40:56 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:40:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:40:57 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:40:57 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fb05d6c9821a7ff3202d9e895fb6991a0fa4c38ef84cdbc4591b3445cd648`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84280fff4fea28aa843e6a641415aab2d3928e6aaf87af8d67821bab8025f36`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159665277aa747535ac0cff9e0dc6314c4c383a85ee04b2d1f17818654b63c`  
		Last Modified: Fri, 16 Jun 2023 07:44:59 GMT  
		Size: 474.7 MB (474720057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89a67fa322a3e521fc8dc5c99232a7a41e02e13a6c47ae4d7985d399d66a998`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e24e99cfadeef9f01a724dc3755ec15aa3e858d15148a23a3568a66e1c4bb92e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565918872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaa0b3ec6bb44464adfcddd9edbd344d7bcf7fad111b6d553c0ea09176ed08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:32:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:32:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:32:33 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:51 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:54 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:54 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792070497b5a1fcfaf1913ff3d564f760d3d96a745fc1ef620012f7a0a555b6`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d772ec46d67513a5e4aebe575fab628faacaa0166947e648bb0446599807a`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4e455d43050e6bd09f037fd4fc6816b68d47e7b4ba7c1424fb88000e99a124`  
		Last Modified: Fri, 16 Jun 2023 04:36:34 GMT  
		Size: 474.7 MB (474720017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e760faff74565c71228c73ddf609bfee9f5691119c4f10525f03562956d3fc1`  
		Last Modified: Fri, 16 Jun 2023 04:36:19 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-scala_2.12-java11`

```console
$ docker pull flink@sha256:34e8e2990ee21b27854e50e24e4bfeeda473d2e580054b9c884e4f488c6b3557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:59394226f0392d43c8621eef0c4a1f82bfc57ce54b1947e50298ca009e30558c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569873610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f030983e366e8027e68675cf6aaeaf8ca2d5b0125fd5fab1bef93ca834dea6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:40:07 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:40:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:40:07 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:40:55 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:40:56 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:40:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:40:57 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:40:57 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fb05d6c9821a7ff3202d9e895fb6991a0fa4c38ef84cdbc4591b3445cd648`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84280fff4fea28aa843e6a641415aab2d3928e6aaf87af8d67821bab8025f36`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159665277aa747535ac0cff9e0dc6314c4c383a85ee04b2d1f17818654b63c`  
		Last Modified: Fri, 16 Jun 2023 07:44:59 GMT  
		Size: 474.7 MB (474720057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89a67fa322a3e521fc8dc5c99232a7a41e02e13a6c47ae4d7985d399d66a998`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e24e99cfadeef9f01a724dc3755ec15aa3e858d15148a23a3568a66e1c4bb92e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565918872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaa0b3ec6bb44464adfcddd9edbd344d7bcf7fad111b6d553c0ea09176ed08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:32:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:32:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:32:33 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:51 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:54 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:54 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792070497b5a1fcfaf1913ff3d564f760d3d96a745fc1ef620012f7a0a555b6`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d772ec46d67513a5e4aebe575fab628faacaa0166947e648bb0446599807a`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4e455d43050e6bd09f037fd4fc6816b68d47e7b4ba7c1424fb88000e99a124`  
		Last Modified: Fri, 16 Jun 2023 04:36:34 GMT  
		Size: 474.7 MB (474720017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e760faff74565c71228c73ddf609bfee9f5691119c4f10525f03562956d3fc1`  
		Last Modified: Fri, 16 Jun 2023 04:36:19 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16-scala_2.12-java8`

```console
$ docker pull flink@sha256:7acc4a846999e1c6b0e7c8e9b39cf7a2c623b466bc3002d16443056d12ece0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:15e6fc6c8be28040da94f0daaefc0b3395faafa9e454a9ec528fa79bec023bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.0 MB (565044644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e23e69aea0c29721a2b7568615c7000b0b8affd06fa051274a24aeee3e66f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:39:25 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:39:26 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:39:26 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:39:26 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:39:26 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:58 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:58 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:58 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38988a938e7c26e5210e4ec3ffa60e16a62af570cbc5e92efb36afa2beef7539`  
		Last Modified: Fri, 16 Jun 2023 07:44:08 GMT  
		Size: 4.6 KB (4611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01fbbf7a7ec70fdc13dded3e45e158e0ccc31430f5e1a74e3c808ee6b0238ce`  
		Last Modified: Fri, 16 Jun 2023 07:44:09 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cb21082895019bba7b17bfa447f37da20a66fa83a6b33f00ab9371a1f62275`  
		Last Modified: Fri, 16 Jun 2023 07:44:28 GMT  
		Size: 474.7 MB (474720129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46106bb814865f3b9804933650885edf1c7b1950442a0403954e3c3ae8eaa5f`  
		Last Modified: Fri, 16 Jun 2023 07:44:09 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:b4542098079bcb108d4c01403b764df4e9f913d0d77e92521ae2ba290df842d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561730485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5b4d10b10af0fc537cd5b917add9b25fe9e097afea6f5e26413d17393826d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:45 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:45 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:45 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:45 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:45 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:27 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:30 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:30 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:30 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bf50c5781afffe889f5f00aec6ccb6e9472e4604bb156b3e27363040130d4`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff268c2a1badc9a52a1501cbb84aa76b4847aa5a5721dfd1682a60a2da7ef515`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f4c5b5ed54a1c4720d5a2748758c8e235fd6ca5c3927ea3882bc1c59871572`  
		Last Modified: Fri, 16 Jun 2023 04:36:06 GMT  
		Size: 474.7 MB (474720039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45714402c098a84e9ed4c71a16e96dfa895f58ab4d9ab0d848652b4f567cf4e`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.2`

```console
$ docker pull flink@sha256:34e8e2990ee21b27854e50e24e4bfeeda473d2e580054b9c884e4f488c6b3557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.2` - linux; amd64

```console
$ docker pull flink@sha256:59394226f0392d43c8621eef0c4a1f82bfc57ce54b1947e50298ca009e30558c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569873610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f030983e366e8027e68675cf6aaeaf8ca2d5b0125fd5fab1bef93ca834dea6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:40:07 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:40:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:40:07 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:40:55 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:40:56 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:40:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:40:57 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:40:57 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fb05d6c9821a7ff3202d9e895fb6991a0fa4c38ef84cdbc4591b3445cd648`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84280fff4fea28aa843e6a641415aab2d3928e6aaf87af8d67821bab8025f36`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159665277aa747535ac0cff9e0dc6314c4c383a85ee04b2d1f17818654b63c`  
		Last Modified: Fri, 16 Jun 2023 07:44:59 GMT  
		Size: 474.7 MB (474720057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89a67fa322a3e521fc8dc5c99232a7a41e02e13a6c47ae4d7985d399d66a998`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.2` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e24e99cfadeef9f01a724dc3755ec15aa3e858d15148a23a3568a66e1c4bb92e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565918872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaa0b3ec6bb44464adfcddd9edbd344d7bcf7fad111b6d553c0ea09176ed08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:32:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:32:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:32:33 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:51 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:54 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:54 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792070497b5a1fcfaf1913ff3d564f760d3d96a745fc1ef620012f7a0a555b6`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d772ec46d67513a5e4aebe575fab628faacaa0166947e648bb0446599807a`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4e455d43050e6bd09f037fd4fc6816b68d47e7b4ba7c1424fb88000e99a124`  
		Last Modified: Fri, 16 Jun 2023 04:36:34 GMT  
		Size: 474.7 MB (474720017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e760faff74565c71228c73ddf609bfee9f5691119c4f10525f03562956d3fc1`  
		Last Modified: Fri, 16 Jun 2023 04:36:19 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.2-java11`

```console
$ docker pull flink@sha256:34e8e2990ee21b27854e50e24e4bfeeda473d2e580054b9c884e4f488c6b3557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.2-java11` - linux; amd64

```console
$ docker pull flink@sha256:59394226f0392d43c8621eef0c4a1f82bfc57ce54b1947e50298ca009e30558c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569873610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f030983e366e8027e68675cf6aaeaf8ca2d5b0125fd5fab1bef93ca834dea6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:40:07 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:40:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:40:07 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:40:55 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:40:56 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:40:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:40:57 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:40:57 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fb05d6c9821a7ff3202d9e895fb6991a0fa4c38ef84cdbc4591b3445cd648`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84280fff4fea28aa843e6a641415aab2d3928e6aaf87af8d67821bab8025f36`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159665277aa747535ac0cff9e0dc6314c4c383a85ee04b2d1f17818654b63c`  
		Last Modified: Fri, 16 Jun 2023 07:44:59 GMT  
		Size: 474.7 MB (474720057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89a67fa322a3e521fc8dc5c99232a7a41e02e13a6c47ae4d7985d399d66a998`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.2-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e24e99cfadeef9f01a724dc3755ec15aa3e858d15148a23a3568a66e1c4bb92e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565918872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaa0b3ec6bb44464adfcddd9edbd344d7bcf7fad111b6d553c0ea09176ed08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:32:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:32:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:32:33 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:51 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:54 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:54 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792070497b5a1fcfaf1913ff3d564f760d3d96a745fc1ef620012f7a0a555b6`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d772ec46d67513a5e4aebe575fab628faacaa0166947e648bb0446599807a`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4e455d43050e6bd09f037fd4fc6816b68d47e7b4ba7c1424fb88000e99a124`  
		Last Modified: Fri, 16 Jun 2023 04:36:34 GMT  
		Size: 474.7 MB (474720017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e760faff74565c71228c73ddf609bfee9f5691119c4f10525f03562956d3fc1`  
		Last Modified: Fri, 16 Jun 2023 04:36:19 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.2-java8`

```console
$ docker pull flink@sha256:7acc4a846999e1c6b0e7c8e9b39cf7a2c623b466bc3002d16443056d12ece0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.2-java8` - linux; amd64

```console
$ docker pull flink@sha256:15e6fc6c8be28040da94f0daaefc0b3395faafa9e454a9ec528fa79bec023bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.0 MB (565044644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e23e69aea0c29721a2b7568615c7000b0b8affd06fa051274a24aeee3e66f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:39:25 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:39:26 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:39:26 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:39:26 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:39:26 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:58 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:58 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:58 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38988a938e7c26e5210e4ec3ffa60e16a62af570cbc5e92efb36afa2beef7539`  
		Last Modified: Fri, 16 Jun 2023 07:44:08 GMT  
		Size: 4.6 KB (4611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01fbbf7a7ec70fdc13dded3e45e158e0ccc31430f5e1a74e3c808ee6b0238ce`  
		Last Modified: Fri, 16 Jun 2023 07:44:09 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cb21082895019bba7b17bfa447f37da20a66fa83a6b33f00ab9371a1f62275`  
		Last Modified: Fri, 16 Jun 2023 07:44:28 GMT  
		Size: 474.7 MB (474720129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46106bb814865f3b9804933650885edf1c7b1950442a0403954e3c3ae8eaa5f`  
		Last Modified: Fri, 16 Jun 2023 07:44:09 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.2-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:b4542098079bcb108d4c01403b764df4e9f913d0d77e92521ae2ba290df842d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561730485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5b4d10b10af0fc537cd5b917add9b25fe9e097afea6f5e26413d17393826d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:45 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:45 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:45 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:45 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:45 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:27 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:30 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:30 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:30 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bf50c5781afffe889f5f00aec6ccb6e9472e4604bb156b3e27363040130d4`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff268c2a1badc9a52a1501cbb84aa76b4847aa5a5721dfd1682a60a2da7ef515`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f4c5b5ed54a1c4720d5a2748758c8e235fd6ca5c3927ea3882bc1c59871572`  
		Last Modified: Fri, 16 Jun 2023 04:36:06 GMT  
		Size: 474.7 MB (474720039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45714402c098a84e9ed4c71a16e96dfa895f58ab4d9ab0d848652b4f567cf4e`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.2-scala_2.12`

```console
$ docker pull flink@sha256:34e8e2990ee21b27854e50e24e4bfeeda473d2e580054b9c884e4f488c6b3557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.2-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:59394226f0392d43c8621eef0c4a1f82bfc57ce54b1947e50298ca009e30558c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569873610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f030983e366e8027e68675cf6aaeaf8ca2d5b0125fd5fab1bef93ca834dea6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:40:07 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:40:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:40:07 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:40:55 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:40:56 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:40:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:40:57 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:40:57 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fb05d6c9821a7ff3202d9e895fb6991a0fa4c38ef84cdbc4591b3445cd648`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84280fff4fea28aa843e6a641415aab2d3928e6aaf87af8d67821bab8025f36`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159665277aa747535ac0cff9e0dc6314c4c383a85ee04b2d1f17818654b63c`  
		Last Modified: Fri, 16 Jun 2023 07:44:59 GMT  
		Size: 474.7 MB (474720057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89a67fa322a3e521fc8dc5c99232a7a41e02e13a6c47ae4d7985d399d66a998`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.2-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e24e99cfadeef9f01a724dc3755ec15aa3e858d15148a23a3568a66e1c4bb92e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565918872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaa0b3ec6bb44464adfcddd9edbd344d7bcf7fad111b6d553c0ea09176ed08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:32:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:32:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:32:33 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:51 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:54 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:54 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792070497b5a1fcfaf1913ff3d564f760d3d96a745fc1ef620012f7a0a555b6`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d772ec46d67513a5e4aebe575fab628faacaa0166947e648bb0446599807a`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4e455d43050e6bd09f037fd4fc6816b68d47e7b4ba7c1424fb88000e99a124`  
		Last Modified: Fri, 16 Jun 2023 04:36:34 GMT  
		Size: 474.7 MB (474720017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e760faff74565c71228c73ddf609bfee9f5691119c4f10525f03562956d3fc1`  
		Last Modified: Fri, 16 Jun 2023 04:36:19 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.2-scala_2.12-java11`

```console
$ docker pull flink@sha256:34e8e2990ee21b27854e50e24e4bfeeda473d2e580054b9c884e4f488c6b3557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.2-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:59394226f0392d43c8621eef0c4a1f82bfc57ce54b1947e50298ca009e30558c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569873610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f030983e366e8027e68675cf6aaeaf8ca2d5b0125fd5fab1bef93ca834dea6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:40:06 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:40:07 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:40:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:40:07 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:40:55 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:40:56 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:40:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:40:57 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:40:57 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fb05d6c9821a7ff3202d9e895fb6991a0fa4c38ef84cdbc4591b3445cd648`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84280fff4fea28aa843e6a641415aab2d3928e6aaf87af8d67821bab8025f36`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159665277aa747535ac0cff9e0dc6314c4c383a85ee04b2d1f17818654b63c`  
		Last Modified: Fri, 16 Jun 2023 07:44:59 GMT  
		Size: 474.7 MB (474720057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89a67fa322a3e521fc8dc5c99232a7a41e02e13a6c47ae4d7985d399d66a998`  
		Last Modified: Fri, 16 Jun 2023 07:44:40 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.2-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:e24e99cfadeef9f01a724dc3755ec15aa3e858d15148a23a3568a66e1c4bb92e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565918872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaa0b3ec6bb44464adfcddd9edbd344d7bcf7fad111b6d553c0ea09176ed08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:32:33 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:32:33 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:32:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:32:33 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:51 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:54 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:54 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:54 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792070497b5a1fcfaf1913ff3d564f760d3d96a745fc1ef620012f7a0a555b6`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 4.7 KB (4653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d772ec46d67513a5e4aebe575fab628faacaa0166947e648bb0446599807a`  
		Last Modified: Fri, 16 Jun 2023 04:36:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4e455d43050e6bd09f037fd4fc6816b68d47e7b4ba7c1424fb88000e99a124`  
		Last Modified: Fri, 16 Jun 2023 04:36:34 GMT  
		Size: 474.7 MB (474720017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e760faff74565c71228c73ddf609bfee9f5691119c4f10525f03562956d3fc1`  
		Last Modified: Fri, 16 Jun 2023 04:36:19 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.16.2-scala_2.12-java8`

```console
$ docker pull flink@sha256:7acc4a846999e1c6b0e7c8e9b39cf7a2c623b466bc3002d16443056d12ece0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.16.2-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:15e6fc6c8be28040da94f0daaefc0b3395faafa9e454a9ec528fa79bec023bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.0 MB (565044644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e23e69aea0c29721a2b7568615c7000b0b8affd06fa051274a24aeee3e66f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:39:25 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:39:26 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:39:26 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:39:26 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:39:26 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:56 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:58 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:58 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:58 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38988a938e7c26e5210e4ec3ffa60e16a62af570cbc5e92efb36afa2beef7539`  
		Last Modified: Fri, 16 Jun 2023 07:44:08 GMT  
		Size: 4.6 KB (4611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01fbbf7a7ec70fdc13dded3e45e158e0ccc31430f5e1a74e3c808ee6b0238ce`  
		Last Modified: Fri, 16 Jun 2023 07:44:09 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cb21082895019bba7b17bfa447f37da20a66fa83a6b33f00ab9371a1f62275`  
		Last Modified: Fri, 16 Jun 2023 07:44:28 GMT  
		Size: 474.7 MB (474720129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46106bb814865f3b9804933650885edf1c7b1950442a0403954e3c3ae8eaa5f`  
		Last Modified: Fri, 16 Jun 2023 07:44:09 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.16.2-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:b4542098079bcb108d4c01403b764df4e9f913d0d77e92521ae2ba290df842d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561730485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5b4d10b10af0fc537cd5b917add9b25fe9e097afea6f5e26413d17393826d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:45 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.16.2/flink-1.16.2-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:45 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:45 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:45 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:45 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:32:27 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:32:30 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:32:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:32:30 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:32:30 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bf50c5781afffe889f5f00aec6ccb6e9472e4604bb156b3e27363040130d4`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff268c2a1badc9a52a1501cbb84aa76b4847aa5a5721dfd1682a60a2da7ef515`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f4c5b5ed54a1c4720d5a2748758c8e235fd6ca5c3927ea3882bc1c59871572`  
		Last Modified: Fri, 16 Jun 2023 04:36:06 GMT  
		Size: 474.7 MB (474720039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45714402c098a84e9ed4c71a16e96dfa895f58ab4d9ab0d848652b4f567cf4e`  
		Last Modified: Fri, 16 Jun 2023 04:35:50 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17-java11`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17-java11` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17-java8`

```console
$ docker pull flink@sha256:46d63098587bc00a50366a3e379f96565f6588350aed5b08d4c21f89b3c722e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17-java8` - linux; amd64

```console
$ docker pull flink@sha256:0f32825c03fe4e785eb6f2c48bf8170f71a236aeef558c182fc2a906d804ae6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.9 MB (559923788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da975bf31332940ad81e5f3c7bdac5cd679d3ac250a707f4c8c0588b8a73d431`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:36:23 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:36:23 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:36:23 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:37:47 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:37:48 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:37:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:37:48 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:37:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f606220b74e3261078c14a32356d4e8c052164b64d2c0da64bc8506892868f0`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba33d0507027fc7246cd2748814222429e8a26cb8f0cd4040de85c0611dcbc8`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441622c3fb0c1105e523bf208e81bfdd317efa802baee6bf14e449eb6d5673b3`  
		Last Modified: Fri, 16 Jun 2023 07:43:05 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b073ff4fac1f02861d343a1b23ff7dbde24c09d3a9678399fbbca19fe8f6946e`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:de5db56f7c7ef7cdeee8a0e27ddc4fbaa8a2d92679b0018716fa0e976f2f864c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.6 MB (556609729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fd79adb964bd0786c973bdc49d70799424a4be68414086ac87e96863c1e26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:30:28 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:30:28 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:30:28 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:30:52 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:30:55 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:30:55 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:30:55 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10b9ed7700a1585f7a2d4298c156fa19c245dde21391358fe78f1ac397eb12`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b824c82647310850ef8284384b1d6e55829439ac5428a0a1df3aa2352a672d13`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cba62d1b7bda1e0d277014274acd346821dee82dd4da45372fad6b4b404655`  
		Last Modified: Fri, 16 Jun 2023 04:34:50 GMT  
		Size: 469.6 MB (469599284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ebe6f0032f165787c2852a6823951b3179ea3c0bd2692cd9e582cb8936d2b`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17-scala_2.12`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17-scala_2.12-java11`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17-scala_2.12-java8`

```console
$ docker pull flink@sha256:46d63098587bc00a50366a3e379f96565f6588350aed5b08d4c21f89b3c722e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:0f32825c03fe4e785eb6f2c48bf8170f71a236aeef558c182fc2a906d804ae6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.9 MB (559923788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da975bf31332940ad81e5f3c7bdac5cd679d3ac250a707f4c8c0588b8a73d431`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:36:23 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:36:23 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:36:23 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:37:47 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:37:48 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:37:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:37:48 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:37:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f606220b74e3261078c14a32356d4e8c052164b64d2c0da64bc8506892868f0`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba33d0507027fc7246cd2748814222429e8a26cb8f0cd4040de85c0611dcbc8`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441622c3fb0c1105e523bf208e81bfdd317efa802baee6bf14e449eb6d5673b3`  
		Last Modified: Fri, 16 Jun 2023 07:43:05 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b073ff4fac1f02861d343a1b23ff7dbde24c09d3a9678399fbbca19fe8f6946e`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:de5db56f7c7ef7cdeee8a0e27ddc4fbaa8a2d92679b0018716fa0e976f2f864c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.6 MB (556609729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fd79adb964bd0786c973bdc49d70799424a4be68414086ac87e96863c1e26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:30:28 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:30:28 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:30:28 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:30:52 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:30:55 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:30:55 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:30:55 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10b9ed7700a1585f7a2d4298c156fa19c245dde21391358fe78f1ac397eb12`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b824c82647310850ef8284384b1d6e55829439ac5428a0a1df3aa2352a672d13`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cba62d1b7bda1e0d277014274acd346821dee82dd4da45372fad6b4b404655`  
		Last Modified: Fri, 16 Jun 2023 04:34:50 GMT  
		Size: 469.6 MB (469599284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ebe6f0032f165787c2852a6823951b3179ea3c0bd2692cd9e582cb8936d2b`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17.1`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17.1` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17.1` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17.1-java11`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17.1-java11` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17.1-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17.1-java8`

```console
$ docker pull flink@sha256:46d63098587bc00a50366a3e379f96565f6588350aed5b08d4c21f89b3c722e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17.1-java8` - linux; amd64

```console
$ docker pull flink@sha256:0f32825c03fe4e785eb6f2c48bf8170f71a236aeef558c182fc2a906d804ae6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.9 MB (559923788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da975bf31332940ad81e5f3c7bdac5cd679d3ac250a707f4c8c0588b8a73d431`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:36:23 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:36:23 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:36:23 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:37:47 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:37:48 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:37:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:37:48 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:37:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f606220b74e3261078c14a32356d4e8c052164b64d2c0da64bc8506892868f0`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba33d0507027fc7246cd2748814222429e8a26cb8f0cd4040de85c0611dcbc8`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441622c3fb0c1105e523bf208e81bfdd317efa802baee6bf14e449eb6d5673b3`  
		Last Modified: Fri, 16 Jun 2023 07:43:05 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b073ff4fac1f02861d343a1b23ff7dbde24c09d3a9678399fbbca19fe8f6946e`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17.1-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:de5db56f7c7ef7cdeee8a0e27ddc4fbaa8a2d92679b0018716fa0e976f2f864c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.6 MB (556609729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fd79adb964bd0786c973bdc49d70799424a4be68414086ac87e96863c1e26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:30:28 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:30:28 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:30:28 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:30:52 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:30:55 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:30:55 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:30:55 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10b9ed7700a1585f7a2d4298c156fa19c245dde21391358fe78f1ac397eb12`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b824c82647310850ef8284384b1d6e55829439ac5428a0a1df3aa2352a672d13`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cba62d1b7bda1e0d277014274acd346821dee82dd4da45372fad6b4b404655`  
		Last Modified: Fri, 16 Jun 2023 04:34:50 GMT  
		Size: 469.6 MB (469599284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ebe6f0032f165787c2852a6823951b3179ea3c0bd2692cd9e582cb8936d2b`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17.1-scala_2.12`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17.1-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17.1-scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17.1-scala_2.12-java11`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17.1-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17.1-scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.17.1-scala_2.12-java8`

```console
$ docker pull flink@sha256:46d63098587bc00a50366a3e379f96565f6588350aed5b08d4c21f89b3c722e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:1.17.1-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:0f32825c03fe4e785eb6f2c48bf8170f71a236aeef558c182fc2a906d804ae6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.9 MB (559923788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da975bf31332940ad81e5f3c7bdac5cd679d3ac250a707f4c8c0588b8a73d431`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:36:23 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:36:23 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:36:23 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:37:47 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:37:48 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:37:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:37:48 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:37:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f606220b74e3261078c14a32356d4e8c052164b64d2c0da64bc8506892868f0`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba33d0507027fc7246cd2748814222429e8a26cb8f0cd4040de85c0611dcbc8`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441622c3fb0c1105e523bf208e81bfdd317efa802baee6bf14e449eb6d5673b3`  
		Last Modified: Fri, 16 Jun 2023 07:43:05 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b073ff4fac1f02861d343a1b23ff7dbde24c09d3a9678399fbbca19fe8f6946e`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:1.17.1-scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:de5db56f7c7ef7cdeee8a0e27ddc4fbaa8a2d92679b0018716fa0e976f2f864c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.6 MB (556609729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fd79adb964bd0786c973bdc49d70799424a4be68414086ac87e96863c1e26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:30:28 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:30:28 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:30:28 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:30:52 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:30:55 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:30:55 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:30:55 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10b9ed7700a1585f7a2d4298c156fa19c245dde21391358fe78f1ac397eb12`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b824c82647310850ef8284384b1d6e55829439ac5428a0a1df3aa2352a672d13`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cba62d1b7bda1e0d277014274acd346821dee82dd4da45372fad6b4b404655`  
		Last Modified: Fri, 16 Jun 2023 04:34:50 GMT  
		Size: 469.6 MB (469599284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ebe6f0032f165787c2852a6823951b3179ea3c0bd2692cd9e582cb8936d2b`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:java11`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:java11` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:java8`

```console
$ docker pull flink@sha256:46d63098587bc00a50366a3e379f96565f6588350aed5b08d4c21f89b3c722e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:java8` - linux; amd64

```console
$ docker pull flink@sha256:0f32825c03fe4e785eb6f2c48bf8170f71a236aeef558c182fc2a906d804ae6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.9 MB (559923788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da975bf31332940ad81e5f3c7bdac5cd679d3ac250a707f4c8c0588b8a73d431`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:36:23 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:36:23 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:36:23 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:37:47 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:37:48 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:37:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:37:48 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:37:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f606220b74e3261078c14a32356d4e8c052164b64d2c0da64bc8506892868f0`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba33d0507027fc7246cd2748814222429e8a26cb8f0cd4040de85c0611dcbc8`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441622c3fb0c1105e523bf208e81bfdd317efa802baee6bf14e449eb6d5673b3`  
		Last Modified: Fri, 16 Jun 2023 07:43:05 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b073ff4fac1f02861d343a1b23ff7dbde24c09d3a9678399fbbca19fe8f6946e`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:de5db56f7c7ef7cdeee8a0e27ddc4fbaa8a2d92679b0018716fa0e976f2f864c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.6 MB (556609729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fd79adb964bd0786c973bdc49d70799424a4be68414086ac87e96863c1e26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:30:28 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:30:28 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:30:28 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:30:52 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:30:55 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:30:55 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:30:55 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10b9ed7700a1585f7a2d4298c156fa19c245dde21391358fe78f1ac397eb12`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b824c82647310850ef8284384b1d6e55829439ac5428a0a1df3aa2352a672d13`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cba62d1b7bda1e0d277014274acd346821dee82dd4da45372fad6b4b404655`  
		Last Modified: Fri, 16 Jun 2023 04:34:50 GMT  
		Size: 469.6 MB (469599284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ebe6f0032f165787c2852a6823951b3179ea3c0bd2692cd9e582cb8936d2b`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:latest`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:latest` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:latest` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:scala_2.12`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:scala_2.12` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:scala_2.12-java11`

```console
$ docker pull flink@sha256:7570e49e3a07e556e7e53912458fbf64abecc4030313649a3c34d28e1cf7572b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:d2a5ab99218eb1a04584187d9572decb90dedc67f2e979869eea7b1f96b5541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564752827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b08a86592f4ace8080cb5b3ccfd9c7e9860945aaf5d0ee07a07d5c44378d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:38:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:38:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:38:15 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:38:15 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:38:15 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:38:15 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:38:16 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:39:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:39:18 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:39:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:39:18 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:39:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906feab3d1ffe6f8d194544b36d7e399e813e77a2df6678380a6b4c5a18aec2f`  
		Last Modified: Fri, 16 Jun 2023 02:22:53 GMT  
		Size: 46.7 MB (46666394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358731a04ce4ffb43ea1162e0684391b355b508420d45ae7921eb8cab9c10db`  
		Last Modified: Fri, 16 Jun 2023 02:22:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c61567212e1a07092b9840035f45a3fa33832a2bd5d85dea1d7cb01c24326b5`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.7 MB (4653385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f03ed8b25d3289995068600633a0628a31b1ff784868bae2a6a1d7f3028884`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 900.5 KB (900510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d686e68e74af3b8af27b72fbc1bffd84fc008b348f986e9480d5a94ccffa7f78`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703cf41f94f8465a3f183315bd4d6e0752e2526bfdd5e3c1358f3d173685bb52`  
		Last Modified: Fri, 16 Jun 2023 07:43:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d10549278433464149596044ddc78429419b692e6138523e73cec952fd4e7`  
		Last Modified: Fri, 16 Jun 2023 07:43:40 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25a3b7fdd1352ac6b0c037483f09c73099749abd3eb0229ef4f1000fb503f9`  
		Last Modified: Fri, 16 Jun 2023 07:43:22 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:scala_2.12-java11` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:36d52d694ab6a9aacb4c81cad14ccc90504329fe69737acfbcb46d79a0b1c076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560798135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c58f4a3ce2f4295c34725af47da67dcff319ceacdd4c5836aca583a060fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:47:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 04:31:09 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:09 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:31:21 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:31:21 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:31:21 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:31:21 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:31:22 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:31:40 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:31:43 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:31:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:31:43 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:31:43 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e5488ab47450fbd12fc724963811b99580bfe1e5f44267a03736f0adea506b`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 45.0 MB (45009402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbf45ca92463ef69ad1ef7fb34bb5123ea7a7fdfe4f745d3728e89f260617`  
		Last Modified: Fri, 16 Jun 2023 02:51:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6ae7b1fc86f213da9482aa55734c3ae6e2d80409c2f7bb9d9bb66e3cc41b6`  
		Last Modified: Fri, 16 Jun 2023 04:35:09 GMT  
		Size: 4.5 MB (4503341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f960c2851ffc20cca7fad5cd39d33641a3addf74bcd8292dc3ea8dec7da529`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e77b80c4a53380dbae4183dcdddde3a4cb1a229e24e3726aa2738222386e390`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32abe9a11abb615d48abdcee264b835d950ca055ee4749afad9cc8a3036f3aa`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f53bafeb9ed97f5709cda3470624dc10a4eda5e22ba793409355339ae5c3cca`  
		Last Modified: Fri, 16 Jun 2023 04:35:22 GMT  
		Size: 469.6 MB (469599283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee9978af3def89216e90b7d66216fb84e32545e98fcc976534cc9da30fe7e30`  
		Last Modified: Fri, 16 Jun 2023 04:35:07 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:scala_2.12-java8`

```console
$ docker pull flink@sha256:46d63098587bc00a50366a3e379f96565f6588350aed5b08d4c21f89b3c722e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:0f32825c03fe4e785eb6f2c48bf8170f71a236aeef558c182fc2a906d804ae6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.9 MB (559923788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da975bf31332940ad81e5f3c7bdac5cd679d3ac250a707f4c8c0588b8a73d431`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:16:14 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:16:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 07:36:16 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 07:36:16 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 07:36:22 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 07:36:22 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 07:36:23 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 07:36:23 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 07:36:23 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 07:37:47 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 07:37:48 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 07:37:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:37:48 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 07:37:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fb34ffad82f009b11a40d67c4bca9c7e33975241162068dbcb75d1eaa13833`  
		Last Modified: Fri, 16 Jun 2023 02:21:33 GMT  
		Size: 41.8 MB (41837276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeaab81d6793eb15e0eaa14a2708947e106d494d25ecdecc6b80daac1ef9e38`  
		Last Modified: Fri, 16 Jun 2023 02:21:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbf8990ee6a4248732e46bb746da1902c7b3514830fdd82a482d0d8245a15b5`  
		Last Modified: Fri, 16 Jun 2023 07:42:49 GMT  
		Size: 4.7 MB (4653466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1492aaa849c582405ceeaa1e754ec692fc277ac47abe907b1796a90885200e1`  
		Last Modified: Fri, 16 Jun 2023 07:42:47 GMT  
		Size: 900.5 KB (900509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f606220b74e3261078c14a32356d4e8c052164b64d2c0da64bc8506892868f0`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 4.6 KB (4610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba33d0507027fc7246cd2748814222429e8a26cb8f0cd4040de85c0611dcbc8`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441622c3fb0c1105e523bf208e81bfdd317efa802baee6bf14e449eb6d5673b3`  
		Last Modified: Fri, 16 Jun 2023 07:43:05 GMT  
		Size: 469.6 MB (469599274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b073ff4fac1f02861d343a1b23ff7dbde24c09d3a9678399fbbca19fe8f6946e`  
		Last Modified: Fri, 16 Jun 2023 07:42:46 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:scala_2.12-java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:de5db56f7c7ef7cdeee8a0e27ddc4fbaa8a2d92679b0018716fa0e976f2f864c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.6 MB (556609729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fd79adb964bd0786c973bdc49d70799424a4be68414086ac87e96863c1e26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:02 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Fri, 16 Jun 2023 02:46:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f8e440273c8feb3fcfaca88ba18fec291deae18a548adde8a37cd1db08107b95';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='e58e017012838ae4f0db78293e3246cc09958e6ea9a2393c5947ec003bf736dd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ba5f8141a16722e39576bf42b69d2b8ebf95fc2c05441e3200f609af4dd9f1ea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b6fdfe32085a884c11b31f66aa67ac62811df7112fb6fb08beea61376a86fbb4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 16 Jun 2023 02:46:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 16 Jun 2023 04:30:08 GMT
RUN set -ex;   apt-get update;   apt-get -y install gpg libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:30:08 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 04:30:28 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.17.1/flink-1.17.1-bin-scala_2.12.tgz.asc GPG_KEY=8D56AE6E7082699A4870750EA4E8C4C05EE6861F CHECK_GPG=true
# Fri, 16 Jun 2023 04:30:28 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 16 Jun 2023 04:30:28 GMT
ENV PATH=/opt/flink/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:30:28 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 16 Jun 2023 04:30:28 GMT
WORKDIR /opt/flink
# Fri, 16 Jun 2023 04:30:52 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;     sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Fri, 16 Jun 2023 04:30:55 GMT
COPY file:ab8cf5711c2ee73018994cee7133a7f61b2e5fca388abbb79b5eac61bf7f4fa3 in / 
# Fri, 16 Jun 2023 04:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 04:30:55 GMT
EXPOSE 6123 8081
# Fri, 16 Jun 2023 04:30:55 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758993a3c85d74bffdc80b9035995ec8b7a4b79576d8e1925d801a9921a1816c`  
		Last Modified: Fri, 16 Jun 2023 02:50:26 GMT  
		Size: 40.8 MB (40821060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91641ece49fc295e09c2c99a12a883b9d0f25de569029840315401fc03ca2ff9`  
		Last Modified: Fri, 16 Jun 2023 02:50:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36887c557bf1b3f65211b5b9da2df3ff0387d3613fea06272936016bbdafd0`  
		Last Modified: Fri, 16 Jun 2023 04:34:38 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef31176f6f3702b461f96c77f1b94d767455df7b991991be329aa152aafe9b95`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 835.4 KB (835391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10b9ed7700a1585f7a2d4298c156fa19c245dde21391358fe78f1ac397eb12`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 4.6 KB (4649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b824c82647310850ef8284384b1d6e55829439ac5428a0a1df3aa2352a672d13`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cba62d1b7bda1e0d277014274acd346821dee82dd4da45372fad6b4b404655`  
		Last Modified: Fri, 16 Jun 2023 04:34:50 GMT  
		Size: 469.6 MB (469599284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ebe6f0032f165787c2852a6823951b3179ea3c0bd2692cd9e582cb8936d2b`  
		Last Modified: Fri, 16 Jun 2023 04:34:35 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
