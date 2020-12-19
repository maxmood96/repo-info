<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `flink`

-	[`flink:1.10`](#flink110)
-	[`flink:1.10.2`](#flink1102)
-	[`flink:1.10.2-scala_2.11`](#flink1102-scala_211)
-	[`flink:1.10.2-scala_2.12`](#flink1102-scala_212)
-	[`flink:1.10-scala_2.11`](#flink110-scala_211)
-	[`flink:1.10-scala_2.12`](#flink110-scala_212)
-	[`flink:1.11`](#flink111)
-	[`flink:1.11.3`](#flink1113)
-	[`flink:1.11.3-java11`](#flink1113-java11)
-	[`flink:1.11.3-java8`](#flink1113-java8)
-	[`flink:1.11.3-scala_2.11`](#flink1113-scala_211)
-	[`flink:1.11.3-scala_2.11-java11`](#flink1113-scala_211-java11)
-	[`flink:1.11.3-scala_2.11-java8`](#flink1113-scala_211-java8)
-	[`flink:1.11.3-scala_2.12`](#flink1113-scala_212)
-	[`flink:1.11.3-scala_2.12-java11`](#flink1113-scala_212-java11)
-	[`flink:1.11.3-scala_2.12-java8`](#flink1113-scala_212-java8)
-	[`flink:1.11-java11`](#flink111-java11)
-	[`flink:1.11-java8`](#flink111-java8)
-	[`flink:1.11-scala_2.11`](#flink111-scala_211)
-	[`flink:1.11-scala_2.11-java11`](#flink111-scala_211-java11)
-	[`flink:1.11-scala_2.11-java8`](#flink111-scala_211-java8)
-	[`flink:1.11-scala_2.12`](#flink111-scala_212)
-	[`flink:1.11-scala_2.12-java11`](#flink111-scala_212-java11)
-	[`flink:1.11-scala_2.12-java8`](#flink111-scala_212-java8)

## `flink:1.10`

```console
$ docker pull flink@sha256:c6ee4be967ca86d8d99bdfc18fcaf84bbd18bf7a23c389919bfb9afdc1cb084b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.10` - linux; amd64

```console
$ docker pull flink@sha256:b3c67697b022518d7883c750d9b80085ae5146ee5fd77932c6e8dc2e263e1cf6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396696411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eafb4efa8034de7d1810d902ea4847094930b19317211b9f6c95fcc6334cb9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 07:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 07:04:51 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 07:06:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 10 Sep 2020 07:06:15 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 07:06:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 10 Sep 2020 07:06:16 GMT
ENV JAVA_VERSION=8u265
# Thu, 10 Sep 2020 07:06:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 11 Sep 2020 04:39:48 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 04:39:49 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Sep 2020 04:39:50 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 11 Sep 2020 04:46:32 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.10.2/flink-1.10.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.10.2/flink-1.10.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Fri, 11 Sep 2020 04:46:32 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 11 Sep 2020 04:46:33 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 04:46:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 11 Sep 2020 04:46:34 GMT
WORKDIR /opt/flink
# Fri, 11 Sep 2020 04:47:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Fri, 11 Sep 2020 04:47:01 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Fri, 11 Sep 2020 04:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Sep 2020 04:47:02 GMT
EXPOSE 6123 8081
# Fri, 11 Sep 2020 04:47:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e126169501d71bbbd0d3c8d9f35836c41660869fe8432ac606341ed21f7adb`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 7.8 MB (7811567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af28a55c3f320826db8df3146a2c198f9042877ef679f9e32210aa9a7fac9ef`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 10.0 MB (9996317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9777c2d5c29a7fd4b5c4efe0fa2ad6176ca9c5430163ca0c620d94eca56baae`  
		Last Modified: Thu, 10 Sep 2020 07:13:52 GMT  
		Size: 5.5 MB (5529417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248106993db7bc5baf0074c4304fce24d8101cc2046349605cdc01be0d3a92a`  
		Last Modified: Thu, 10 Sep 2020 07:15:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ab5b5b3ee2a4b98345c100cb380be8b776c69c9f3f92b9a1170d3227ce92`  
		Last Modified: Thu, 10 Sep 2020 07:15:33 GMT  
		Size: 40.3 MB (40334785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ec319497407f530849074f16a373c8a94499623c409fbbbfbb750f15e2e47f`  
		Last Modified: Fri, 11 Sep 2020 04:47:48 GMT  
		Size: 531.1 KB (531074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c66f47ca7e4db1dbb44a4105fdb65753ece62c8b0b454faf905f4fea4d3b9e4`  
		Last Modified: Fri, 11 Sep 2020 04:47:47 GMT  
		Size: 900.5 KB (900515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57212cf7bba3d7f400712ed99da7632ccdbf368a3cf9a7419b76db8582365083`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 4.6 KB (4604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a5ad4475dafc4ceab5fc0e544de9d6d28fdb1d304f58af2fd36882c0d7b7bc`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c53333ce4f79cbaac4364c019626d7fdde7fa2d9ff27c241327a324afe63637`  
		Last Modified: Fri, 11 Sep 2020 04:49:44 GMT  
		Size: 281.2 MB (281190205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d05ccc3c14bd8df7e6387889e3e53834c60bd52f94569cd5ed144913e7452`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.10.2`

```console
$ docker pull flink@sha256:c6ee4be967ca86d8d99bdfc18fcaf84bbd18bf7a23c389919bfb9afdc1cb084b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.10.2` - linux; amd64

```console
$ docker pull flink@sha256:b3c67697b022518d7883c750d9b80085ae5146ee5fd77932c6e8dc2e263e1cf6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396696411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eafb4efa8034de7d1810d902ea4847094930b19317211b9f6c95fcc6334cb9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 07:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 07:04:51 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 07:06:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 10 Sep 2020 07:06:15 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 07:06:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 10 Sep 2020 07:06:16 GMT
ENV JAVA_VERSION=8u265
# Thu, 10 Sep 2020 07:06:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 11 Sep 2020 04:39:48 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 04:39:49 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Sep 2020 04:39:50 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 11 Sep 2020 04:46:32 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.10.2/flink-1.10.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.10.2/flink-1.10.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Fri, 11 Sep 2020 04:46:32 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 11 Sep 2020 04:46:33 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 04:46:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 11 Sep 2020 04:46:34 GMT
WORKDIR /opt/flink
# Fri, 11 Sep 2020 04:47:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Fri, 11 Sep 2020 04:47:01 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Fri, 11 Sep 2020 04:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Sep 2020 04:47:02 GMT
EXPOSE 6123 8081
# Fri, 11 Sep 2020 04:47:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e126169501d71bbbd0d3c8d9f35836c41660869fe8432ac606341ed21f7adb`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 7.8 MB (7811567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af28a55c3f320826db8df3146a2c198f9042877ef679f9e32210aa9a7fac9ef`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 10.0 MB (9996317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9777c2d5c29a7fd4b5c4efe0fa2ad6176ca9c5430163ca0c620d94eca56baae`  
		Last Modified: Thu, 10 Sep 2020 07:13:52 GMT  
		Size: 5.5 MB (5529417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248106993db7bc5baf0074c4304fce24d8101cc2046349605cdc01be0d3a92a`  
		Last Modified: Thu, 10 Sep 2020 07:15:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ab5b5b3ee2a4b98345c100cb380be8b776c69c9f3f92b9a1170d3227ce92`  
		Last Modified: Thu, 10 Sep 2020 07:15:33 GMT  
		Size: 40.3 MB (40334785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ec319497407f530849074f16a373c8a94499623c409fbbbfbb750f15e2e47f`  
		Last Modified: Fri, 11 Sep 2020 04:47:48 GMT  
		Size: 531.1 KB (531074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c66f47ca7e4db1dbb44a4105fdb65753ece62c8b0b454faf905f4fea4d3b9e4`  
		Last Modified: Fri, 11 Sep 2020 04:47:47 GMT  
		Size: 900.5 KB (900515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57212cf7bba3d7f400712ed99da7632ccdbf368a3cf9a7419b76db8582365083`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 4.6 KB (4604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a5ad4475dafc4ceab5fc0e544de9d6d28fdb1d304f58af2fd36882c0d7b7bc`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c53333ce4f79cbaac4364c019626d7fdde7fa2d9ff27c241327a324afe63637`  
		Last Modified: Fri, 11 Sep 2020 04:49:44 GMT  
		Size: 281.2 MB (281190205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d05ccc3c14bd8df7e6387889e3e53834c60bd52f94569cd5ed144913e7452`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.10.2-scala_2.11`

```console
$ docker pull flink@sha256:0c9f448249e0ceb331ed4ea0c368b843f3f3d940ae9eaab23b195b301492546d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.10.2-scala_2.11` - linux; amd64

```console
$ docker pull flink@sha256:77f2af67da0b9ca9a6b69d6f8d5259df598a49339e78ec084ff36707a3db7317
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.0 MB (405988064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c8c9b966c51d16d4629fd4de8206816679a133e9cc32c180567e41b2d8bc4e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 07:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 07:04:51 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 07:06:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 10 Sep 2020 07:06:15 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 07:06:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 10 Sep 2020 07:06:16 GMT
ENV JAVA_VERSION=8u265
# Thu, 10 Sep 2020 07:06:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 11 Sep 2020 04:39:48 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 04:39:49 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Sep 2020 04:39:50 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 11 Sep 2020 04:47:07 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.10.2/flink-1.10.2-bin-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.10.2/flink-1.10.2-bin-scala_2.11.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Fri, 11 Sep 2020 04:47:07 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 11 Sep 2020 04:47:07 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 04:47:08 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 11 Sep 2020 04:47:08 GMT
WORKDIR /opt/flink
# Fri, 11 Sep 2020 04:47:26 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Fri, 11 Sep 2020 04:47:26 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Fri, 11 Sep 2020 04:47:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Sep 2020 04:47:27 GMT
EXPOSE 6123 8081
# Fri, 11 Sep 2020 04:47:27 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e126169501d71bbbd0d3c8d9f35836c41660869fe8432ac606341ed21f7adb`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 7.8 MB (7811567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af28a55c3f320826db8df3146a2c198f9042877ef679f9e32210aa9a7fac9ef`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 10.0 MB (9996317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9777c2d5c29a7fd4b5c4efe0fa2ad6176ca9c5430163ca0c620d94eca56baae`  
		Last Modified: Thu, 10 Sep 2020 07:13:52 GMT  
		Size: 5.5 MB (5529417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248106993db7bc5baf0074c4304fce24d8101cc2046349605cdc01be0d3a92a`  
		Last Modified: Thu, 10 Sep 2020 07:15:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ab5b5b3ee2a4b98345c100cb380be8b776c69c9f3f92b9a1170d3227ce92`  
		Last Modified: Thu, 10 Sep 2020 07:15:33 GMT  
		Size: 40.3 MB (40334785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ec319497407f530849074f16a373c8a94499623c409fbbbfbb750f15e2e47f`  
		Last Modified: Fri, 11 Sep 2020 04:47:48 GMT  
		Size: 531.1 KB (531074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c66f47ca7e4db1dbb44a4105fdb65753ece62c8b0b454faf905f4fea4d3b9e4`  
		Last Modified: Fri, 11 Sep 2020 04:47:47 GMT  
		Size: 900.5 KB (900515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ee5505a72d04496dbb2d3b776b2877c21ef54112a8a1ea35870716e4be12b`  
		Last Modified: Fri, 11 Sep 2020 04:49:53 GMT  
		Size: 4.6 KB (4604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af3679def1d9983914fd173cb884d890d388e3cd90ebeb5bb7ded929673cf7`  
		Last Modified: Fri, 11 Sep 2020 04:49:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ef95fc0cdaa2ae092cb7b5193b020d9325fe0f9edb8933115d87123b893c5f`  
		Last Modified: Fri, 11 Sep 2020 04:50:08 GMT  
		Size: 290.5 MB (290481858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0eb1be3dddbe8a3f30c6d63574e63d75245dcc3751a107b694df8a7b010cb77`  
		Last Modified: Fri, 11 Sep 2020 04:49:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.10.2-scala_2.12`

```console
$ docker pull flink@sha256:c6ee4be967ca86d8d99bdfc18fcaf84bbd18bf7a23c389919bfb9afdc1cb084b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.10.2-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:b3c67697b022518d7883c750d9b80085ae5146ee5fd77932c6e8dc2e263e1cf6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396696411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eafb4efa8034de7d1810d902ea4847094930b19317211b9f6c95fcc6334cb9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 07:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 07:04:51 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 07:06:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 10 Sep 2020 07:06:15 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 07:06:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 10 Sep 2020 07:06:16 GMT
ENV JAVA_VERSION=8u265
# Thu, 10 Sep 2020 07:06:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 11 Sep 2020 04:39:48 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 04:39:49 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Sep 2020 04:39:50 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 11 Sep 2020 04:46:32 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.10.2/flink-1.10.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.10.2/flink-1.10.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Fri, 11 Sep 2020 04:46:32 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 11 Sep 2020 04:46:33 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 04:46:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 11 Sep 2020 04:46:34 GMT
WORKDIR /opt/flink
# Fri, 11 Sep 2020 04:47:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Fri, 11 Sep 2020 04:47:01 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Fri, 11 Sep 2020 04:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Sep 2020 04:47:02 GMT
EXPOSE 6123 8081
# Fri, 11 Sep 2020 04:47:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e126169501d71bbbd0d3c8d9f35836c41660869fe8432ac606341ed21f7adb`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 7.8 MB (7811567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af28a55c3f320826db8df3146a2c198f9042877ef679f9e32210aa9a7fac9ef`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 10.0 MB (9996317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9777c2d5c29a7fd4b5c4efe0fa2ad6176ca9c5430163ca0c620d94eca56baae`  
		Last Modified: Thu, 10 Sep 2020 07:13:52 GMT  
		Size: 5.5 MB (5529417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248106993db7bc5baf0074c4304fce24d8101cc2046349605cdc01be0d3a92a`  
		Last Modified: Thu, 10 Sep 2020 07:15:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ab5b5b3ee2a4b98345c100cb380be8b776c69c9f3f92b9a1170d3227ce92`  
		Last Modified: Thu, 10 Sep 2020 07:15:33 GMT  
		Size: 40.3 MB (40334785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ec319497407f530849074f16a373c8a94499623c409fbbbfbb750f15e2e47f`  
		Last Modified: Fri, 11 Sep 2020 04:47:48 GMT  
		Size: 531.1 KB (531074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c66f47ca7e4db1dbb44a4105fdb65753ece62c8b0b454faf905f4fea4d3b9e4`  
		Last Modified: Fri, 11 Sep 2020 04:47:47 GMT  
		Size: 900.5 KB (900515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57212cf7bba3d7f400712ed99da7632ccdbf368a3cf9a7419b76db8582365083`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 4.6 KB (4604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a5ad4475dafc4ceab5fc0e544de9d6d28fdb1d304f58af2fd36882c0d7b7bc`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c53333ce4f79cbaac4364c019626d7fdde7fa2d9ff27c241327a324afe63637`  
		Last Modified: Fri, 11 Sep 2020 04:49:44 GMT  
		Size: 281.2 MB (281190205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d05ccc3c14bd8df7e6387889e3e53834c60bd52f94569cd5ed144913e7452`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.10-scala_2.11`

```console
$ docker pull flink@sha256:0c9f448249e0ceb331ed4ea0c368b843f3f3d940ae9eaab23b195b301492546d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.10-scala_2.11` - linux; amd64

```console
$ docker pull flink@sha256:77f2af67da0b9ca9a6b69d6f8d5259df598a49339e78ec084ff36707a3db7317
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.0 MB (405988064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c8c9b966c51d16d4629fd4de8206816679a133e9cc32c180567e41b2d8bc4e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 07:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 07:04:51 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 07:06:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 10 Sep 2020 07:06:15 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 07:06:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 10 Sep 2020 07:06:16 GMT
ENV JAVA_VERSION=8u265
# Thu, 10 Sep 2020 07:06:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 11 Sep 2020 04:39:48 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 04:39:49 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Sep 2020 04:39:50 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 11 Sep 2020 04:47:07 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.10.2/flink-1.10.2-bin-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.10.2/flink-1.10.2-bin-scala_2.11.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Fri, 11 Sep 2020 04:47:07 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 11 Sep 2020 04:47:07 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 04:47:08 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 11 Sep 2020 04:47:08 GMT
WORKDIR /opt/flink
# Fri, 11 Sep 2020 04:47:26 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Fri, 11 Sep 2020 04:47:26 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Fri, 11 Sep 2020 04:47:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Sep 2020 04:47:27 GMT
EXPOSE 6123 8081
# Fri, 11 Sep 2020 04:47:27 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e126169501d71bbbd0d3c8d9f35836c41660869fe8432ac606341ed21f7adb`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 7.8 MB (7811567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af28a55c3f320826db8df3146a2c198f9042877ef679f9e32210aa9a7fac9ef`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 10.0 MB (9996317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9777c2d5c29a7fd4b5c4efe0fa2ad6176ca9c5430163ca0c620d94eca56baae`  
		Last Modified: Thu, 10 Sep 2020 07:13:52 GMT  
		Size: 5.5 MB (5529417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248106993db7bc5baf0074c4304fce24d8101cc2046349605cdc01be0d3a92a`  
		Last Modified: Thu, 10 Sep 2020 07:15:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ab5b5b3ee2a4b98345c100cb380be8b776c69c9f3f92b9a1170d3227ce92`  
		Last Modified: Thu, 10 Sep 2020 07:15:33 GMT  
		Size: 40.3 MB (40334785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ec319497407f530849074f16a373c8a94499623c409fbbbfbb750f15e2e47f`  
		Last Modified: Fri, 11 Sep 2020 04:47:48 GMT  
		Size: 531.1 KB (531074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c66f47ca7e4db1dbb44a4105fdb65753ece62c8b0b454faf905f4fea4d3b9e4`  
		Last Modified: Fri, 11 Sep 2020 04:47:47 GMT  
		Size: 900.5 KB (900515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ee5505a72d04496dbb2d3b776b2877c21ef54112a8a1ea35870716e4be12b`  
		Last Modified: Fri, 11 Sep 2020 04:49:53 GMT  
		Size: 4.6 KB (4604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af3679def1d9983914fd173cb884d890d388e3cd90ebeb5bb7ded929673cf7`  
		Last Modified: Fri, 11 Sep 2020 04:49:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ef95fc0cdaa2ae092cb7b5193b020d9325fe0f9edb8933115d87123b893c5f`  
		Last Modified: Fri, 11 Sep 2020 04:50:08 GMT  
		Size: 290.5 MB (290481858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0eb1be3dddbe8a3f30c6d63574e63d75245dcc3751a107b694df8a7b010cb77`  
		Last Modified: Fri, 11 Sep 2020 04:49:53 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.10-scala_2.12`

```console
$ docker pull flink@sha256:c6ee4be967ca86d8d99bdfc18fcaf84bbd18bf7a23c389919bfb9afdc1cb084b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.10-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:b3c67697b022518d7883c750d9b80085ae5146ee5fd77932c6e8dc2e263e1cf6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396696411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eafb4efa8034de7d1810d902ea4847094930b19317211b9f6c95fcc6334cb9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 07:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 07:04:51 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 07:06:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 10 Sep 2020 07:06:15 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Sep 2020 07:06:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 10 Sep 2020 07:06:16 GMT
ENV JAVA_VERSION=8u265
# Thu, 10 Sep 2020 07:06:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 11 Sep 2020 04:39:48 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 04:39:49 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Sep 2020 04:39:50 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Fri, 11 Sep 2020 04:46:32 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.10.2/flink-1.10.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.10.2/flink-1.10.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Fri, 11 Sep 2020 04:46:32 GMT
ENV FLINK_HOME=/opt/flink
# Fri, 11 Sep 2020 04:46:33 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 04:46:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Fri, 11 Sep 2020 04:46:34 GMT
WORKDIR /opt/flink
# Fri, 11 Sep 2020 04:47:01 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Fri, 11 Sep 2020 04:47:01 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Fri, 11 Sep 2020 04:47:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Sep 2020 04:47:02 GMT
EXPOSE 6123 8081
# Fri, 11 Sep 2020 04:47:02 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e126169501d71bbbd0d3c8d9f35836c41660869fe8432ac606341ed21f7adb`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 7.8 MB (7811567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af28a55c3f320826db8df3146a2c198f9042877ef679f9e32210aa9a7fac9ef`  
		Last Modified: Thu, 10 Sep 2020 01:15:23 GMT  
		Size: 10.0 MB (9996317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9777c2d5c29a7fd4b5c4efe0fa2ad6176ca9c5430163ca0c620d94eca56baae`  
		Last Modified: Thu, 10 Sep 2020 07:13:52 GMT  
		Size: 5.5 MB (5529417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248106993db7bc5baf0074c4304fce24d8101cc2046349605cdc01be0d3a92a`  
		Last Modified: Thu, 10 Sep 2020 07:15:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74ab5b5b3ee2a4b98345c100cb380be8b776c69c9f3f92b9a1170d3227ce92`  
		Last Modified: Thu, 10 Sep 2020 07:15:33 GMT  
		Size: 40.3 MB (40334785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ec319497407f530849074f16a373c8a94499623c409fbbbfbb750f15e2e47f`  
		Last Modified: Fri, 11 Sep 2020 04:47:48 GMT  
		Size: 531.1 KB (531074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c66f47ca7e4db1dbb44a4105fdb65753ece62c8b0b454faf905f4fea4d3b9e4`  
		Last Modified: Fri, 11 Sep 2020 04:47:47 GMT  
		Size: 900.5 KB (900515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57212cf7bba3d7f400712ed99da7632ccdbf368a3cf9a7419b76db8582365083`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 4.6 KB (4604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a5ad4475dafc4ceab5fc0e544de9d6d28fdb1d304f58af2fd36882c0d7b7bc`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c53333ce4f79cbaac4364c019626d7fdde7fa2d9ff27c241327a324afe63637`  
		Last Modified: Fri, 11 Sep 2020 04:49:44 GMT  
		Size: 281.2 MB (281190205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d05ccc3c14bd8df7e6387889e3e53834c60bd52f94569cd5ed144913e7452`  
		Last Modified: Fri, 11 Sep 2020 04:49:29 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11`

```console
$ docker pull flink@sha256:1fe4fb22a2a5ae9239914f36b97413a4cdd7a37d9655353684c8abd6f20b1af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11` - linux; amd64

```console
$ docker pull flink@sha256:eee9eea7c2ff50edbc11fa27eba03894095e50dae4729af0a5a66bbec0b24d1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.3 MB (428317814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d54adbf2442c82263a1ec952fd95a57e68a3d549c05ba20680f3d508950a6f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 10 Dec 2020 14:20:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:20:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:20:32 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:20:32 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:20:32 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:20:33 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:20:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:20:34 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:20:58 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:20:58 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:20:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:20:58 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:20:58 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745520d3d21cb70ca09af29670ced791449e9f1c925f19d7a1fa775482344a8d`  
		Last Modified: Thu, 10 Dec 2020 14:33:12 GMT  
		Size: 531.0 KB (531047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce52e15aefc2da2b033c790a29c6c4b10df43c8b41ed3f271ad85a32e92f1c`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6950aa5565b1c4d953fad973c75842a8454280fe9234b0bbd8cc29c2a1091b78`  
		Last Modified: Thu, 10 Dec 2020 14:33:09 GMT  
		Size: 4.6 KB (4605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2ad2520eb4ce86b90321860a27d2957ecc67a8d5ca072f9c2579bdcf232607`  
		Last Modified: Thu, 10 Dec 2020 14:33:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595912530b851d64c8297201f563df10b138235d2f59cd1263d3a767acaf4242`  
		Last Modified: Thu, 10 Dec 2020 14:33:29 GMT  
		Size: 311.8 MB (311843174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c84529d07eaf31912713e8626e9188f9a34fe58c83455afe6f6365ad99485b`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11.3`

**does not exist** (yet?)

## `flink:1.11.3-java11`

**does not exist** (yet?)

## `flink:1.11.3-java8`

**does not exist** (yet?)

## `flink:1.11.3-scala_2.11`

**does not exist** (yet?)

## `flink:1.11.3-scala_2.11-java11`

**does not exist** (yet?)

## `flink:1.11.3-scala_2.11-java8`

**does not exist** (yet?)

## `flink:1.11.3-scala_2.12`

**does not exist** (yet?)

## `flink:1.11.3-scala_2.12-java11`

**does not exist** (yet?)

## `flink:1.11.3-scala_2.12-java8`

**does not exist** (yet?)

## `flink:1.11-java11`

```console
$ docker pull flink@sha256:48e60ba29ff2b51353896df1156e2c1684ff01f2dfdb94ca5e746c304c56c67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11-java11` - linux; amd64

```console
$ docker pull flink@sha256:3588352fa3806e0ddcb0c2a332a9a26b8e9bddc0251508a29e81f88e147ad8a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429143159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac02a3445698fb965af50fda819a67dfbb3ffbd21001acdfbb8efa0decb39cf0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:06:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 19 Nov 2020 03:06:46 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:06:47 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:06:47 GMT
ENV JAVA_VERSION=11.0.9.1
# Thu, 19 Nov 2020 03:06:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 10 Dec 2020 14:21:35 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:21:35 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:21:37 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:21:37 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:21:37 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:21:37 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:21:38 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:21:38 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:21:53 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:21:53 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:21:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:21:53 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:21:53 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82f5f9d54ce3640bdd7fcc0d226e74fe7869827f6450e0b8ad9fde5c3f5cc1a`  
		Last Modified: Thu, 19 Nov 2020 03:12:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712ae6b46d2c8f29bd509911354f731a94291f2ea2a21edadd60e67146a9a06`  
		Last Modified: Thu, 19 Nov 2020 03:12:25 GMT  
		Size: 42.1 MB (42126684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c681653b5f90689b8d067cb2cefd4adef5d265a09f242357300d4d998c764f4`  
		Last Modified: Thu, 10 Dec 2020 14:34:17 GMT  
		Size: 531.1 KB (531061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb530aafdb6277357dfe5cdaf77658304cd2e9d75d5152b94d085ce49f819a5`  
		Last Modified: Thu, 10 Dec 2020 14:34:15 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da0448f12907ead2ddcc677b96d5b51958e6e0d0d2260b088ffe73ae54d2a76`  
		Last Modified: Thu, 10 Dec 2020 14:34:14 GMT  
		Size: 4.6 KB (4605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f255b4f43b756e873f342cd74630eafeceb78272f1cdb5ac94beed08174190`  
		Last Modified: Thu, 10 Dec 2020 14:34:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d086b0ad1b784cf0c375c107e53c95b19c4358e0d54d7529d5c4d3353d2bedeb`  
		Last Modified: Thu, 10 Dec 2020 14:34:37 GMT  
		Size: 311.8 MB (311843176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833224f59622dc4871066274743b1dfd6961e3415b647f6eefd205a7df0a75e4`  
		Last Modified: Thu, 10 Dec 2020 14:34:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11-java8`

```console
$ docker pull flink@sha256:1fe4fb22a2a5ae9239914f36b97413a4cdd7a37d9655353684c8abd6f20b1af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11-java8` - linux; amd64

```console
$ docker pull flink@sha256:eee9eea7c2ff50edbc11fa27eba03894095e50dae4729af0a5a66bbec0b24d1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.3 MB (428317814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d54adbf2442c82263a1ec952fd95a57e68a3d549c05ba20680f3d508950a6f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 10 Dec 2020 14:20:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:20:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:20:32 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:20:32 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:20:32 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:20:33 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:20:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:20:34 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:20:58 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:20:58 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:20:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:20:58 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:20:58 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745520d3d21cb70ca09af29670ced791449e9f1c925f19d7a1fa775482344a8d`  
		Last Modified: Thu, 10 Dec 2020 14:33:12 GMT  
		Size: 531.0 KB (531047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce52e15aefc2da2b033c790a29c6c4b10df43c8b41ed3f271ad85a32e92f1c`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6950aa5565b1c4d953fad973c75842a8454280fe9234b0bbd8cc29c2a1091b78`  
		Last Modified: Thu, 10 Dec 2020 14:33:09 GMT  
		Size: 4.6 KB (4605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2ad2520eb4ce86b90321860a27d2957ecc67a8d5ca072f9c2579bdcf232607`  
		Last Modified: Thu, 10 Dec 2020 14:33:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595912530b851d64c8297201f563df10b138235d2f59cd1263d3a767acaf4242`  
		Last Modified: Thu, 10 Dec 2020 14:33:29 GMT  
		Size: 311.8 MB (311843174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c84529d07eaf31912713e8626e9188f9a34fe58c83455afe6f6365ad99485b`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11-scala_2.11`

```console
$ docker pull flink@sha256:2c1f2877b19a4311b0911256fff187029a83330b47c2cff5a4201b5f3078d76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11-scala_2.11` - linux; amd64

```console
$ docker pull flink@sha256:b7a46e6eeee948aa46d3a856b66ad8bdb5fb7f409901fb8d95c16952e7762724
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.7 MB (437702014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b8ce8aa26b80be1f642ef5f7231bbbac9dea3de871bf0b02e8193083b0b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 10 Dec 2020 14:20:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:20:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:20:32 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:21:05 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:21:05 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:21:06 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:21:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:21:07 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:21:24 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:21:24 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:21:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:21:24 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:21:24 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745520d3d21cb70ca09af29670ced791449e9f1c925f19d7a1fa775482344a8d`  
		Last Modified: Thu, 10 Dec 2020 14:33:12 GMT  
		Size: 531.0 KB (531047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce52e15aefc2da2b033c790a29c6c4b10df43c8b41ed3f271ad85a32e92f1c`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e4284ec8cf96c80fc42d6b17e6fc63747d638671fd975abc9c70bde02cbf00`  
		Last Modified: Thu, 10 Dec 2020 14:33:45 GMT  
		Size: 4.6 KB (4607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ffa647a49f95c2f65c3b454cc69f9152f9ed7450b60233f0004d0bbe52548a`  
		Last Modified: Thu, 10 Dec 2020 14:33:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc52dab532693bf96bffb3b8b6adcbc546c9990bc921234d6e314d570fc94226`  
		Last Modified: Thu, 10 Dec 2020 14:34:03 GMT  
		Size: 321.2 MB (321227373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0536c0e6f1e36d72325ee0f945ba473de994711714dd4b15b099315b7ad3888`  
		Last Modified: Thu, 10 Dec 2020 14:33:44 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11-scala_2.11-java11`

```console
$ docker pull flink@sha256:240cb35ee8be60894d31dc584e09a239176286cf0b933fc1bcdeb3ad00b3fe64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11-scala_2.11-java11` - linux; amd64

```console
$ docker pull flink@sha256:f0eab25985883a333b4969767db195f732df9984c30ef0120e3e1dce09de68e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.5 MB (438527375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b421b0f63aceb25a5f6c05109f6daf3408589e0133e320d535d03276c80fa4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:06:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 19 Nov 2020 03:06:46 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:06:47 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:06:47 GMT
ENV JAVA_VERSION=11.0.9.1
# Thu, 19 Nov 2020 03:06:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 10 Dec 2020 14:21:35 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:21:35 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:21:37 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:22:00 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:22:00 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:22:00 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:22:01 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:22:01 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:32:17 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:32:17 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:32:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:32:17 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:32:18 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82f5f9d54ce3640bdd7fcc0d226e74fe7869827f6450e0b8ad9fde5c3f5cc1a`  
		Last Modified: Thu, 19 Nov 2020 03:12:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712ae6b46d2c8f29bd509911354f731a94291f2ea2a21edadd60e67146a9a06`  
		Last Modified: Thu, 19 Nov 2020 03:12:25 GMT  
		Size: 42.1 MB (42126684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c681653b5f90689b8d067cb2cefd4adef5d265a09f242357300d4d998c764f4`  
		Last Modified: Thu, 10 Dec 2020 14:34:17 GMT  
		Size: 531.1 KB (531061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb530aafdb6277357dfe5cdaf77658304cd2e9d75d5152b94d085ce49f819a5`  
		Last Modified: Thu, 10 Dec 2020 14:34:15 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b316f062904542137440e44333c2d560308d7e8172274c1c031a3b10bbbbff55`  
		Last Modified: Thu, 10 Dec 2020 14:34:47 GMT  
		Size: 4.6 KB (4606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e7c1e2dcd521698f0bcc8a8aff7c37ea61bb81eba4f9c4e7ebafc18af660a3`  
		Last Modified: Thu, 10 Dec 2020 14:34:47 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9663f9e88f749b4e6bb3d526756ceb1f7ed1362107876f8d8552929140e04252`  
		Last Modified: Thu, 10 Dec 2020 14:35:05 GMT  
		Size: 321.2 MB (321227390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40faae482aafcdb60a8d4f2abb7fe13fa1037c5a3adffeb397138cc98ca38e92`  
		Last Modified: Thu, 10 Dec 2020 14:34:46 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11-scala_2.11-java8`

```console
$ docker pull flink@sha256:2c1f2877b19a4311b0911256fff187029a83330b47c2cff5a4201b5f3078d76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11-scala_2.11-java8` - linux; amd64

```console
$ docker pull flink@sha256:b7a46e6eeee948aa46d3a856b66ad8bdb5fb7f409901fb8d95c16952e7762724
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.7 MB (437702014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b8ce8aa26b80be1f642ef5f7231bbbac9dea3de871bf0b02e8193083b0b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 10 Dec 2020 14:20:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:20:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:20:32 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:21:05 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:21:05 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:21:06 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:21:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:21:07 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:21:24 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:21:24 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:21:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:21:24 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:21:24 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745520d3d21cb70ca09af29670ced791449e9f1c925f19d7a1fa775482344a8d`  
		Last Modified: Thu, 10 Dec 2020 14:33:12 GMT  
		Size: 531.0 KB (531047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce52e15aefc2da2b033c790a29c6c4b10df43c8b41ed3f271ad85a32e92f1c`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e4284ec8cf96c80fc42d6b17e6fc63747d638671fd975abc9c70bde02cbf00`  
		Last Modified: Thu, 10 Dec 2020 14:33:45 GMT  
		Size: 4.6 KB (4607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ffa647a49f95c2f65c3b454cc69f9152f9ed7450b60233f0004d0bbe52548a`  
		Last Modified: Thu, 10 Dec 2020 14:33:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc52dab532693bf96bffb3b8b6adcbc546c9990bc921234d6e314d570fc94226`  
		Last Modified: Thu, 10 Dec 2020 14:34:03 GMT  
		Size: 321.2 MB (321227373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0536c0e6f1e36d72325ee0f945ba473de994711714dd4b15b099315b7ad3888`  
		Last Modified: Thu, 10 Dec 2020 14:33:44 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11-scala_2.12`

```console
$ docker pull flink@sha256:1fe4fb22a2a5ae9239914f36b97413a4cdd7a37d9655353684c8abd6f20b1af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11-scala_2.12` - linux; amd64

```console
$ docker pull flink@sha256:eee9eea7c2ff50edbc11fa27eba03894095e50dae4729af0a5a66bbec0b24d1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.3 MB (428317814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d54adbf2442c82263a1ec952fd95a57e68a3d549c05ba20680f3d508950a6f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 10 Dec 2020 14:20:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:20:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:20:32 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:20:32 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:20:32 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:20:33 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:20:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:20:34 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:20:58 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:20:58 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:20:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:20:58 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:20:58 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745520d3d21cb70ca09af29670ced791449e9f1c925f19d7a1fa775482344a8d`  
		Last Modified: Thu, 10 Dec 2020 14:33:12 GMT  
		Size: 531.0 KB (531047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce52e15aefc2da2b033c790a29c6c4b10df43c8b41ed3f271ad85a32e92f1c`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6950aa5565b1c4d953fad973c75842a8454280fe9234b0bbd8cc29c2a1091b78`  
		Last Modified: Thu, 10 Dec 2020 14:33:09 GMT  
		Size: 4.6 KB (4605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2ad2520eb4ce86b90321860a27d2957ecc67a8d5ca072f9c2579bdcf232607`  
		Last Modified: Thu, 10 Dec 2020 14:33:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595912530b851d64c8297201f563df10b138235d2f59cd1263d3a767acaf4242`  
		Last Modified: Thu, 10 Dec 2020 14:33:29 GMT  
		Size: 311.8 MB (311843174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c84529d07eaf31912713e8626e9188f9a34fe58c83455afe6f6365ad99485b`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11-scala_2.12-java11`

```console
$ docker pull flink@sha256:48e60ba29ff2b51353896df1156e2c1684ff01f2dfdb94ca5e746c304c56c67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11-scala_2.12-java11` - linux; amd64

```console
$ docker pull flink@sha256:3588352fa3806e0ddcb0c2a332a9a26b8e9bddc0251508a29e81f88e147ad8a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429143159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac02a3445698fb965af50fda819a67dfbb3ffbd21001acdfbb8efa0decb39cf0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:06:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 19 Nov 2020 03:06:46 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:06:47 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:06:47 GMT
ENV JAVA_VERSION=11.0.9.1
# Thu, 19 Nov 2020 03:06:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 10 Dec 2020 14:21:35 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:21:35 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:21:37 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:21:37 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:21:37 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:21:37 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:21:38 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:21:38 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:21:53 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:21:53 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:21:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:21:53 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:21:53 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82f5f9d54ce3640bdd7fcc0d226e74fe7869827f6450e0b8ad9fde5c3f5cc1a`  
		Last Modified: Thu, 19 Nov 2020 03:12:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712ae6b46d2c8f29bd509911354f731a94291f2ea2a21edadd60e67146a9a06`  
		Last Modified: Thu, 19 Nov 2020 03:12:25 GMT  
		Size: 42.1 MB (42126684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c681653b5f90689b8d067cb2cefd4adef5d265a09f242357300d4d998c764f4`  
		Last Modified: Thu, 10 Dec 2020 14:34:17 GMT  
		Size: 531.1 KB (531061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb530aafdb6277357dfe5cdaf77658304cd2e9d75d5152b94d085ce49f819a5`  
		Last Modified: Thu, 10 Dec 2020 14:34:15 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da0448f12907ead2ddcc677b96d5b51958e6e0d0d2260b088ffe73ae54d2a76`  
		Last Modified: Thu, 10 Dec 2020 14:34:14 GMT  
		Size: 4.6 KB (4605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f255b4f43b756e873f342cd74630eafeceb78272f1cdb5ac94beed08174190`  
		Last Modified: Thu, 10 Dec 2020 14:34:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d086b0ad1b784cf0c375c107e53c95b19c4358e0d54d7529d5c4d3353d2bedeb`  
		Last Modified: Thu, 10 Dec 2020 14:34:37 GMT  
		Size: 311.8 MB (311843176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833224f59622dc4871066274743b1dfd6961e3415b647f6eefd205a7df0a75e4`  
		Last Modified: Thu, 10 Dec 2020 14:34:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `flink:1.11-scala_2.12-java8`

```console
$ docker pull flink@sha256:1fe4fb22a2a5ae9239914f36b97413a4cdd7a37d9655353684c8abd6f20b1af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:1.11-scala_2.12-java8` - linux; amd64

```console
$ docker pull flink@sha256:eee9eea7c2ff50edbc11fa27eba03894095e50dae4729af0a5a66bbec0b24d1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.3 MB (428317814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d54adbf2442c82263a1ec952fd95a57e68a3d549c05ba20680f3d508950a6f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 10 Dec 2020 14:20:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:20:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:20:32 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:20:32 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.12.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:20:32 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:20:33 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:20:34 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:20:34 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:20:58 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:20:58 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:20:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:20:58 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:20:58 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745520d3d21cb70ca09af29670ced791449e9f1c925f19d7a1fa775482344a8d`  
		Last Modified: Thu, 10 Dec 2020 14:33:12 GMT  
		Size: 531.0 KB (531047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce52e15aefc2da2b033c790a29c6c4b10df43c8b41ed3f271ad85a32e92f1c`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6950aa5565b1c4d953fad973c75842a8454280fe9234b0bbd8cc29c2a1091b78`  
		Last Modified: Thu, 10 Dec 2020 14:33:09 GMT  
		Size: 4.6 KB (4605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2ad2520eb4ce86b90321860a27d2957ecc67a8d5ca072f9c2579bdcf232607`  
		Last Modified: Thu, 10 Dec 2020 14:33:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595912530b851d64c8297201f563df10b138235d2f59cd1263d3a767acaf4242`  
		Last Modified: Thu, 10 Dec 2020 14:33:29 GMT  
		Size: 311.8 MB (311843174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c84529d07eaf31912713e8626e9188f9a34fe58c83455afe6f6365ad99485b`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
