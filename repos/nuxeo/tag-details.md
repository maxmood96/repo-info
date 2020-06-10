<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nuxeo`

-	[`nuxeo:10`](#nuxeo10)
-	[`nuxeo:10.10`](#nuxeo1010)
-	[`nuxeo:7`](#nuxeo7)
-	[`nuxeo:7.10`](#nuxeo710)
-	[`nuxeo:8`](#nuxeo8)
-	[`nuxeo:8.10`](#nuxeo810)
-	[`nuxeo:9`](#nuxeo9)
-	[`nuxeo:9.10`](#nuxeo910)
-	[`nuxeo:FT`](#nuxeoft)
-	[`nuxeo:latest`](#nuxeolatest)
-	[`nuxeo:LTS`](#nuxeolts)
-	[`nuxeo:LTS-2015`](#nuxeolts-2015)
-	[`nuxeo:LTS-2016`](#nuxeolts-2016)
-	[`nuxeo:LTS-2017`](#nuxeolts-2017)
-	[`nuxeo:LTS-2019`](#nuxeolts-2019)

## `nuxeo:10`

```console
$ docker pull nuxeo@sha256:f333cc9073a9e53a6bc5d03f386b87ffdd7ba2b82dc8c998f347dbf8ae347191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:10` - linux; amd64

```console
$ docker pull nuxeo@sha256:7de34322c49c8d2c11937f45650782e4f689397d558da6c2fed3924b0be1b8a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.3 MB (954278556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7540aed573f01c30bbfcd3d71658113ba9405fd7fa6799c97776491b3f704def`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_VERSION=10.10
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Wed, 10 Jun 2020 07:28:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:28:27 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:28:27 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:28:27 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:28:28 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:28:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:28:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:28:29 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:29 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:28:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:28:29 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:28:29 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:28:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3f04d3f97aa937624b5114ac4dd0983466a2e78b211d68d50efe1d42fd169b`  
		Last Modified: Wed, 10 Jun 2020 07:31:22 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e1213818205a50e91ca9af5efcd821775b7240cc3d9c692233904104f7ab5f`  
		Last Modified: Wed, 10 Jun 2020 07:31:40 GMT  
		Size: 355.6 MB (355562058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c3fd3dcd1131659d8baa398f5d3a6376b790c597810d7b5c9342a2f3933fb4`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858a0d6d6b459adad8f2c83610893ebf6b711b4a88302ddb7084dc38168bec3`  
		Last Modified: Wed, 10 Jun 2020 07:31:21 GMT  
		Size: 986.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8fbfc68a90cc72b7f3aab6bf5671bda5ddb5f40dcda9dca22fc390b2aa7cb6`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae3529746a18c5d8522d2c6c0ada87907a2d94dff33ab693fe8f27c1d8c5b3a`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:10.10`

```console
$ docker pull nuxeo@sha256:f333cc9073a9e53a6bc5d03f386b87ffdd7ba2b82dc8c998f347dbf8ae347191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:10.10` - linux; amd64

```console
$ docker pull nuxeo@sha256:7de34322c49c8d2c11937f45650782e4f689397d558da6c2fed3924b0be1b8a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.3 MB (954278556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7540aed573f01c30bbfcd3d71658113ba9405fd7fa6799c97776491b3f704def`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_VERSION=10.10
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Wed, 10 Jun 2020 07:28:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:28:27 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:28:27 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:28:27 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:28:28 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:28:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:28:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:28:29 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:29 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:28:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:28:29 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:28:29 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:28:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3f04d3f97aa937624b5114ac4dd0983466a2e78b211d68d50efe1d42fd169b`  
		Last Modified: Wed, 10 Jun 2020 07:31:22 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e1213818205a50e91ca9af5efcd821775b7240cc3d9c692233904104f7ab5f`  
		Last Modified: Wed, 10 Jun 2020 07:31:40 GMT  
		Size: 355.6 MB (355562058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c3fd3dcd1131659d8baa398f5d3a6376b790c597810d7b5c9342a2f3933fb4`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858a0d6d6b459adad8f2c83610893ebf6b711b4a88302ddb7084dc38168bec3`  
		Last Modified: Wed, 10 Jun 2020 07:31:21 GMT  
		Size: 986.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8fbfc68a90cc72b7f3aab6bf5671bda5ddb5f40dcda9dca22fc390b2aa7cb6`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae3529746a18c5d8522d2c6c0ada87907a2d94dff33ab693fe8f27c1d8c5b3a`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:7`

```console
$ docker pull nuxeo@sha256:4bd27c4d4eef8cc0cea310ed29ca2460dfb0875f718a77a1a6bb9ff82efcacff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:7` - linux; amd64

```console
$ docker pull nuxeo@sha256:d60e44dd8ef92831eae1db0907175927ab9f0888bf7920159235fe9390693999
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1155583275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e723e9da0c1b7590c45f61aeb11e2bd9ae34642bb3f67ed80f1dac7bec44efd3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:24:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libreoffice     libwpd-tools     exiftool     ghostscript  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:24:44 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:24:44 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:24:44 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:24:44 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:24:44 GMT
ARG NUXEO_VERSION=7.10
# Wed, 10 Jun 2020 07:24:45 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip
# Wed, 10 Jun 2020 07:24:45 GMT
ARG NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2
# Wed, 10 Jun 2020 07:24:45 GMT
ENV LAUNCHER_DEBUG=-Djvmcheck=nofail
# Wed, 10 Jun 2020 07:24:46 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:25:08 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh
# Wed, 10 Jun 2020 07:25:17 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:25:18 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:25:18 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:25:18 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:25:19 GMT
COPY file:9560db752e0d728d2bb67749bc399b34de55ac127e1fda9bab6523a33ac2fd8c in / 
# Wed, 10 Jun 2020 07:25:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:25:19 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:25:19 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:25:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea65c3a5ddc3dff080679903f6fb2d3ead6b37412f61e5d213c5c1402e87580`  
		Last Modified: Wed, 10 Jun 2020 07:29:41 GMT  
		Size: 364.9 MB (364906652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee85833495a0b981ee8ac5709d614f07fe1937facc3a5571a3a6b728f5a9570d`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd32a4d90c666457ac6370834bb105839a9d4f966eafffe7bca2dbf823b43a7f`  
		Last Modified: Wed, 10 Jun 2020 07:28:59 GMT  
		Size: 280.5 MB (280457927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50db752aaeda8f664373878ec74c9543779f7c229e28d342e19dea7e3fed5c6c`  
		Last Modified: Wed, 10 Jun 2020 07:29:00 GMT  
		Size: 280.5 MB (280459888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcc7ba2e9e0909d95d3e6d132ed060e2cfcf4c5bb7e9497d97f3fce1538dc27`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d5280313cf2e5d330c52de1454ccf8c6ccd9b33ba6ccb7774284025d479d7`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:7.10`

```console
$ docker pull nuxeo@sha256:4bd27c4d4eef8cc0cea310ed29ca2460dfb0875f718a77a1a6bb9ff82efcacff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:7.10` - linux; amd64

```console
$ docker pull nuxeo@sha256:d60e44dd8ef92831eae1db0907175927ab9f0888bf7920159235fe9390693999
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1155583275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e723e9da0c1b7590c45f61aeb11e2bd9ae34642bb3f67ed80f1dac7bec44efd3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:24:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libreoffice     libwpd-tools     exiftool     ghostscript  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:24:44 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:24:44 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:24:44 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:24:44 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:24:44 GMT
ARG NUXEO_VERSION=7.10
# Wed, 10 Jun 2020 07:24:45 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip
# Wed, 10 Jun 2020 07:24:45 GMT
ARG NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2
# Wed, 10 Jun 2020 07:24:45 GMT
ENV LAUNCHER_DEBUG=-Djvmcheck=nofail
# Wed, 10 Jun 2020 07:24:46 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:25:08 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh
# Wed, 10 Jun 2020 07:25:17 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:25:18 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:25:18 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:25:18 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:25:19 GMT
COPY file:9560db752e0d728d2bb67749bc399b34de55ac127e1fda9bab6523a33ac2fd8c in / 
# Wed, 10 Jun 2020 07:25:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:25:19 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:25:19 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:25:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea65c3a5ddc3dff080679903f6fb2d3ead6b37412f61e5d213c5c1402e87580`  
		Last Modified: Wed, 10 Jun 2020 07:29:41 GMT  
		Size: 364.9 MB (364906652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee85833495a0b981ee8ac5709d614f07fe1937facc3a5571a3a6b728f5a9570d`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd32a4d90c666457ac6370834bb105839a9d4f966eafffe7bca2dbf823b43a7f`  
		Last Modified: Wed, 10 Jun 2020 07:28:59 GMT  
		Size: 280.5 MB (280457927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50db752aaeda8f664373878ec74c9543779f7c229e28d342e19dea7e3fed5c6c`  
		Last Modified: Wed, 10 Jun 2020 07:29:00 GMT  
		Size: 280.5 MB (280459888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcc7ba2e9e0909d95d3e6d132ed060e2cfcf4c5bb7e9497d97f3fce1538dc27`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d5280313cf2e5d330c52de1454ccf8c6ccd9b33ba6ccb7774284025d479d7`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:8`

```console
$ docker pull nuxeo@sha256:0afbad38896ffa77053297b513c0eb3fa223b788a64c23db9335314da815f7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:8` - linux; amd64

```console
$ docker pull nuxeo@sha256:9e232e99bff98e04825bb62b355e7cbb70e4b22469b7a4954ceb4900027a09c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.3 MB (868339214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7bbd27aebd7c520685074f23e6348d151090b2c6510b6dbdeb8e2aef3b8b4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_VERSION=8.10
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_MD5=29e67a19bba54099093b51d892926be1
# Wed, 10 Jun 2020 07:26:48 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:27:06 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:27:10 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:27:11 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:27:12 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:12 GMT
COPY file:bb9febfdc3a76dbd4a80d559b47951e49fca7137ad3b76ce7b7293512f63b257 in / 
# Wed, 10 Jun 2020 07:27:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:27:13 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:27:13 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:27:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9a6a2336962f675461e9e7aa44a84b04137eecdd775a3a3708b91c61feaa9d`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 4.4 KB (4375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9097a9e0663fc7dd040623fc0fd9f4b23cc4bfe65677661265b2df87c0b8e603`  
		Last Modified: Wed, 10 Jun 2020 07:30:06 GMT  
		Size: 269.6 MB (269624430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29bd234bf895ca465967ae016ba60ac8d45c3fe79c5526c24e39c39063a35b4`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 784.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f79f8880662bdf06b09130326054f94b2ca7917528860f8fe7dbe8ba15b053c`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:8.10`

```console
$ docker pull nuxeo@sha256:0afbad38896ffa77053297b513c0eb3fa223b788a64c23db9335314da815f7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:8.10` - linux; amd64

```console
$ docker pull nuxeo@sha256:9e232e99bff98e04825bb62b355e7cbb70e4b22469b7a4954ceb4900027a09c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.3 MB (868339214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7bbd27aebd7c520685074f23e6348d151090b2c6510b6dbdeb8e2aef3b8b4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_VERSION=8.10
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_MD5=29e67a19bba54099093b51d892926be1
# Wed, 10 Jun 2020 07:26:48 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:27:06 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:27:10 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:27:11 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:27:12 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:12 GMT
COPY file:bb9febfdc3a76dbd4a80d559b47951e49fca7137ad3b76ce7b7293512f63b257 in / 
# Wed, 10 Jun 2020 07:27:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:27:13 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:27:13 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:27:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9a6a2336962f675461e9e7aa44a84b04137eecdd775a3a3708b91c61feaa9d`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 4.4 KB (4375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9097a9e0663fc7dd040623fc0fd9f4b23cc4bfe65677661265b2df87c0b8e603`  
		Last Modified: Wed, 10 Jun 2020 07:30:06 GMT  
		Size: 269.6 MB (269624430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29bd234bf895ca465967ae016ba60ac8d45c3fe79c5526c24e39c39063a35b4`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 784.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f79f8880662bdf06b09130326054f94b2ca7917528860f8fe7dbe8ba15b053c`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:9`

```console
$ docker pull nuxeo@sha256:bd28059d624d714cafe032cd5a04961d0951ff512940fc1a6b6e2718cf1344a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:9` - linux; amd64

```console
$ docker pull nuxeo@sha256:ae8f30f639e1e54bfc41e23cb8195f2a58d30708fd4d6cc9e6c10393a8298dc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.9 MB (983873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ee35e12f09473d9e307ed8e77739ebda5c0cf7ab1083904ebb3731a6dd6260`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_VERSION=9.10
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_MD5=327d23bbd5558565694027b11c0dd82a
# Wed, 10 Jun 2020 07:27:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:27:51 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:27:51 GMT
COPY dir:1d4b19e1e35500d85eafcc58364498b9325f119ce19917cefc60c7ad98e600e7 in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:27:52 GMT
COPY file:8f1eb15b3cc87be8784ed6bc39c958a3a06d1e375bda2ce728f297d14d74d526 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:27:52 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:27:53 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:27:53 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:27:53 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:53 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:27:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:27:54 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:27:54 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:27:54 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3243f631f813ea0a0229f20418bb87c07abc29a6d9ef3bda4fbb47360e0c6190`  
		Last Modified: Wed, 10 Jun 2020 07:30:50 GMT  
		Size: 4.4 KB (4376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38686d0e69df5be2a2fac3ee5c106e22d1df8dd3b0fdf467f7d5e04f9a322c3e`  
		Last Modified: Wed, 10 Jun 2020 07:31:09 GMT  
		Size: 385.2 MB (385156121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2fdccc403c0cc96414ef41d1c83a349f7a7efe951b0c28a1a0711ab2ae6dd3`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30fb29b8eae74d3228a57ad10b1db77419169f6f4662d9ec166b5e2b9517709a`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef8d62e84fbfad8a7b305535ff513d2250996b07c92d0e5126827311009e08c`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786c882b4f58cb9626585e4f49867b0e509286015f2427715bf9de2f5268a8a`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:9.10`

```console
$ docker pull nuxeo@sha256:bd28059d624d714cafe032cd5a04961d0951ff512940fc1a6b6e2718cf1344a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:9.10` - linux; amd64

```console
$ docker pull nuxeo@sha256:ae8f30f639e1e54bfc41e23cb8195f2a58d30708fd4d6cc9e6c10393a8298dc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.9 MB (983873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ee35e12f09473d9e307ed8e77739ebda5c0cf7ab1083904ebb3731a6dd6260`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_VERSION=9.10
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_MD5=327d23bbd5558565694027b11c0dd82a
# Wed, 10 Jun 2020 07:27:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:27:51 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:27:51 GMT
COPY dir:1d4b19e1e35500d85eafcc58364498b9325f119ce19917cefc60c7ad98e600e7 in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:27:52 GMT
COPY file:8f1eb15b3cc87be8784ed6bc39c958a3a06d1e375bda2ce728f297d14d74d526 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:27:52 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:27:53 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:27:53 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:27:53 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:53 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:27:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:27:54 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:27:54 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:27:54 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3243f631f813ea0a0229f20418bb87c07abc29a6d9ef3bda4fbb47360e0c6190`  
		Last Modified: Wed, 10 Jun 2020 07:30:50 GMT  
		Size: 4.4 KB (4376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38686d0e69df5be2a2fac3ee5c106e22d1df8dd3b0fdf467f7d5e04f9a322c3e`  
		Last Modified: Wed, 10 Jun 2020 07:31:09 GMT  
		Size: 385.2 MB (385156121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2fdccc403c0cc96414ef41d1c83a349f7a7efe951b0c28a1a0711ab2ae6dd3`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30fb29b8eae74d3228a57ad10b1db77419169f6f4662d9ec166b5e2b9517709a`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef8d62e84fbfad8a7b305535ff513d2250996b07c92d0e5126827311009e08c`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786c882b4f58cb9626585e4f49867b0e509286015f2427715bf9de2f5268a8a`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:FT`

```console
$ docker pull nuxeo@sha256:f333cc9073a9e53a6bc5d03f386b87ffdd7ba2b82dc8c998f347dbf8ae347191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:FT` - linux; amd64

```console
$ docker pull nuxeo@sha256:7de34322c49c8d2c11937f45650782e4f689397d558da6c2fed3924b0be1b8a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.3 MB (954278556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7540aed573f01c30bbfcd3d71658113ba9405fd7fa6799c97776491b3f704def`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_VERSION=10.10
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Wed, 10 Jun 2020 07:28:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:28:27 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:28:27 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:28:27 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:28:28 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:28:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:28:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:28:29 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:29 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:28:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:28:29 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:28:29 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:28:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3f04d3f97aa937624b5114ac4dd0983466a2e78b211d68d50efe1d42fd169b`  
		Last Modified: Wed, 10 Jun 2020 07:31:22 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e1213818205a50e91ca9af5efcd821775b7240cc3d9c692233904104f7ab5f`  
		Last Modified: Wed, 10 Jun 2020 07:31:40 GMT  
		Size: 355.6 MB (355562058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c3fd3dcd1131659d8baa398f5d3a6376b790c597810d7b5c9342a2f3933fb4`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858a0d6d6b459adad8f2c83610893ebf6b711b4a88302ddb7084dc38168bec3`  
		Last Modified: Wed, 10 Jun 2020 07:31:21 GMT  
		Size: 986.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8fbfc68a90cc72b7f3aab6bf5671bda5ddb5f40dcda9dca22fc390b2aa7cb6`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae3529746a18c5d8522d2c6c0ada87907a2d94dff33ab693fe8f27c1d8c5b3a`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:latest`

```console
$ docker pull nuxeo@sha256:f333cc9073a9e53a6bc5d03f386b87ffdd7ba2b82dc8c998f347dbf8ae347191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:latest` - linux; amd64

```console
$ docker pull nuxeo@sha256:7de34322c49c8d2c11937f45650782e4f689397d558da6c2fed3924b0be1b8a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.3 MB (954278556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7540aed573f01c30bbfcd3d71658113ba9405fd7fa6799c97776491b3f704def`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_VERSION=10.10
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Wed, 10 Jun 2020 07:28:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:28:27 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:28:27 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:28:27 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:28:28 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:28:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:28:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:28:29 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:29 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:28:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:28:29 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:28:29 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:28:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3f04d3f97aa937624b5114ac4dd0983466a2e78b211d68d50efe1d42fd169b`  
		Last Modified: Wed, 10 Jun 2020 07:31:22 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e1213818205a50e91ca9af5efcd821775b7240cc3d9c692233904104f7ab5f`  
		Last Modified: Wed, 10 Jun 2020 07:31:40 GMT  
		Size: 355.6 MB (355562058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c3fd3dcd1131659d8baa398f5d3a6376b790c597810d7b5c9342a2f3933fb4`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858a0d6d6b459adad8f2c83610893ebf6b711b4a88302ddb7084dc38168bec3`  
		Last Modified: Wed, 10 Jun 2020 07:31:21 GMT  
		Size: 986.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8fbfc68a90cc72b7f3aab6bf5671bda5ddb5f40dcda9dca22fc390b2aa7cb6`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae3529746a18c5d8522d2c6c0ada87907a2d94dff33ab693fe8f27c1d8c5b3a`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS`

```console
$ docker pull nuxeo@sha256:f333cc9073a9e53a6bc5d03f386b87ffdd7ba2b82dc8c998f347dbf8ae347191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS` - linux; amd64

```console
$ docker pull nuxeo@sha256:7de34322c49c8d2c11937f45650782e4f689397d558da6c2fed3924b0be1b8a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.3 MB (954278556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7540aed573f01c30bbfcd3d71658113ba9405fd7fa6799c97776491b3f704def`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_VERSION=10.10
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Wed, 10 Jun 2020 07:28:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:28:27 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:28:27 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:28:27 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:28:28 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:28:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:28:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:28:29 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:29 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:28:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:28:29 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:28:29 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:28:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3f04d3f97aa937624b5114ac4dd0983466a2e78b211d68d50efe1d42fd169b`  
		Last Modified: Wed, 10 Jun 2020 07:31:22 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e1213818205a50e91ca9af5efcd821775b7240cc3d9c692233904104f7ab5f`  
		Last Modified: Wed, 10 Jun 2020 07:31:40 GMT  
		Size: 355.6 MB (355562058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c3fd3dcd1131659d8baa398f5d3a6376b790c597810d7b5c9342a2f3933fb4`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858a0d6d6b459adad8f2c83610893ebf6b711b4a88302ddb7084dc38168bec3`  
		Last Modified: Wed, 10 Jun 2020 07:31:21 GMT  
		Size: 986.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8fbfc68a90cc72b7f3aab6bf5671bda5ddb5f40dcda9dca22fc390b2aa7cb6`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae3529746a18c5d8522d2c6c0ada87907a2d94dff33ab693fe8f27c1d8c5b3a`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS-2015`

```console
$ docker pull nuxeo@sha256:4bd27c4d4eef8cc0cea310ed29ca2460dfb0875f718a77a1a6bb9ff82efcacff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS-2015` - linux; amd64

```console
$ docker pull nuxeo@sha256:d60e44dd8ef92831eae1db0907175927ab9f0888bf7920159235fe9390693999
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1155583275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e723e9da0c1b7590c45f61aeb11e2bd9ae34642bb3f67ed80f1dac7bec44efd3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:24:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libreoffice     libwpd-tools     exiftool     ghostscript  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:24:44 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:24:44 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:24:44 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:24:44 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:24:44 GMT
ARG NUXEO_VERSION=7.10
# Wed, 10 Jun 2020 07:24:45 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip
# Wed, 10 Jun 2020 07:24:45 GMT
ARG NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2
# Wed, 10 Jun 2020 07:24:45 GMT
ENV LAUNCHER_DEBUG=-Djvmcheck=nofail
# Wed, 10 Jun 2020 07:24:46 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:25:08 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh
# Wed, 10 Jun 2020 07:25:17 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:25:18 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:25:18 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:25:18 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:25:19 GMT
COPY file:9560db752e0d728d2bb67749bc399b34de55ac127e1fda9bab6523a33ac2fd8c in / 
# Wed, 10 Jun 2020 07:25:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:25:19 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:25:19 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:25:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea65c3a5ddc3dff080679903f6fb2d3ead6b37412f61e5d213c5c1402e87580`  
		Last Modified: Wed, 10 Jun 2020 07:29:41 GMT  
		Size: 364.9 MB (364906652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee85833495a0b981ee8ac5709d614f07fe1937facc3a5571a3a6b728f5a9570d`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd32a4d90c666457ac6370834bb105839a9d4f966eafffe7bca2dbf823b43a7f`  
		Last Modified: Wed, 10 Jun 2020 07:28:59 GMT  
		Size: 280.5 MB (280457927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50db752aaeda8f664373878ec74c9543779f7c229e28d342e19dea7e3fed5c6c`  
		Last Modified: Wed, 10 Jun 2020 07:29:00 GMT  
		Size: 280.5 MB (280459888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcc7ba2e9e0909d95d3e6d132ed060e2cfcf4c5bb7e9497d97f3fce1538dc27`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d5280313cf2e5d330c52de1454ccf8c6ccd9b33ba6ccb7774284025d479d7`  
		Last Modified: Wed, 10 Jun 2020 07:28:41 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS-2016`

```console
$ docker pull nuxeo@sha256:0afbad38896ffa77053297b513c0eb3fa223b788a64c23db9335314da815f7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS-2016` - linux; amd64

```console
$ docker pull nuxeo@sha256:9e232e99bff98e04825bb62b355e7cbb70e4b22469b7a4954ceb4900027a09c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.3 MB (868339214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7bbd27aebd7c520685074f23e6348d151090b2c6510b6dbdeb8e2aef3b8b4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_VERSION=8.10
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip
# Wed, 10 Jun 2020 07:26:47 GMT
ARG NUXEO_MD5=29e67a19bba54099093b51d892926be1
# Wed, 10 Jun 2020 07:26:48 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:27:06 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:27:10 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:27:11 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:27:12 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:12 GMT
COPY file:bb9febfdc3a76dbd4a80d559b47951e49fca7137ad3b76ce7b7293512f63b257 in / 
# Wed, 10 Jun 2020 07:27:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:27:13 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:27:13 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:27:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9a6a2336962f675461e9e7aa44a84b04137eecdd775a3a3708b91c61feaa9d`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 4.4 KB (4375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9097a9e0663fc7dd040623fc0fd9f4b23cc4bfe65677661265b2df87c0b8e603`  
		Last Modified: Wed, 10 Jun 2020 07:30:06 GMT  
		Size: 269.6 MB (269624430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29bd234bf895ca465967ae016ba60ac8d45c3fe79c5526c24e39c39063a35b4`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 784.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f79f8880662bdf06b09130326054f94b2ca7917528860f8fe7dbe8ba15b053c`  
		Last Modified: Wed, 10 Jun 2020 07:29:47 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS-2017`

```console
$ docker pull nuxeo@sha256:bd28059d624d714cafe032cd5a04961d0951ff512940fc1a6b6e2718cf1344a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS-2017` - linux; amd64

```console
$ docker pull nuxeo@sha256:ae8f30f639e1e54bfc41e23cb8195f2a58d30708fd4d6cc9e6c10393a8298dc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.9 MB (983873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ee35e12f09473d9e307ed8e77739ebda5c0cf7ab1083904ebb3731a6dd6260`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_VERSION=9.10
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip
# Wed, 10 Jun 2020 07:27:27 GMT
ARG NUXEO_MD5=327d23bbd5558565694027b11c0dd82a
# Wed, 10 Jun 2020 07:27:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:27:51 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:27:51 GMT
COPY dir:1d4b19e1e35500d85eafcc58364498b9325f119ce19917cefc60c7ad98e600e7 in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:27:52 GMT
COPY file:8f1eb15b3cc87be8784ed6bc39c958a3a06d1e375bda2ce728f297d14d74d526 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:27:52 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:27:53 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:27:53 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:27:53 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:27:53 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:27:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:27:54 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:27:54 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:27:54 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3243f631f813ea0a0229f20418bb87c07abc29a6d9ef3bda4fbb47360e0c6190`  
		Last Modified: Wed, 10 Jun 2020 07:30:50 GMT  
		Size: 4.4 KB (4376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38686d0e69df5be2a2fac3ee5c106e22d1df8dd3b0fdf467f7d5e04f9a322c3e`  
		Last Modified: Wed, 10 Jun 2020 07:31:09 GMT  
		Size: 385.2 MB (385156121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2fdccc403c0cc96414ef41d1c83a349f7a7efe951b0c28a1a0711ab2ae6dd3`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30fb29b8eae74d3228a57ad10b1db77419169f6f4662d9ec166b5e2b9517709a`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef8d62e84fbfad8a7b305535ff513d2250996b07c92d0e5126827311009e08c`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786c882b4f58cb9626585e4f49867b0e509286015f2427715bf9de2f5268a8a`  
		Last Modified: Wed, 10 Jun 2020 07:30:49 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS-2019`

```console
$ docker pull nuxeo@sha256:f333cc9073a9e53a6bc5d03f386b87ffdd7ba2b82dc8c998f347dbf8ae347191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS-2019` - linux; amd64

```console
$ docker pull nuxeo@sha256:7de34322c49c8d2c11937f45650782e4f689397d558da6c2fed3924b0be1b8a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.3 MB (954278556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7540aed573f01c30bbfcd3d71658113ba9405fd7fa6799c97776491b3f704def`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:36:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Jun 2020 16:38:41 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:38:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 16:38:42 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 16:38:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Wed, 10 Jun 2020 07:23:09 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Wed, 10 Jun 2020 07:26:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Wed, 10 Jun 2020 07:26:46 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Wed, 10 Jun 2020 07:26:46 GMT
ENV NUXEO_USER=nuxeo
# Wed, 10 Jun 2020 07:26:47 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:26:47 GMT
ENV HOME=/opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_VERSION=10.10
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Wed, 10 Jun 2020 07:28:01 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Wed, 10 Jun 2020 07:28:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Wed, 10 Jun 2020 07:28:27 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Wed, 10 Jun 2020 07:28:27 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Wed, 10 Jun 2020 07:28:27 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Wed, 10 Jun 2020 07:28:28 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Wed, 10 Jun 2020 07:28:28 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Wed, 10 Jun 2020 07:28:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2020 07:28:29 GMT
WORKDIR /opt/nuxeo/server
# Wed, 10 Jun 2020 07:28:29 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Wed, 10 Jun 2020 07:28:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jun 2020 07:28:29 GMT
EXPOSE 8080
# Wed, 10 Jun 2020 07:28:29 GMT
CMD ["nuxeoctl" "console"]
# Wed, 10 Jun 2020 07:28:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1a405f128d35ffb78464f5ac9f15e721e0d205b94360e151d60f32f9b38111`  
		Last Modified: Tue, 09 Jun 2020 16:43:42 GMT  
		Size: 5.3 MB (5284640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197b0f525c2645359f6ff5163a3f2e656358750e87910b9428145509120fc8f2`  
		Last Modified: Tue, 09 Jun 2020 16:45:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133ed18cacaf9f3f44ae673c428b6a4787f51f51e74d4bde7a86cfd6ca8891f`  
		Last Modified: Tue, 09 Jun 2020 16:46:10 GMT  
		Size: 104.4 MB (104442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb0ba216c898525ecf0487a82579e4560ebaf40e9b1122f771069da547dae8`  
		Last Modified: Wed, 10 Jun 2020 07:30:43 GMT  
		Size: 369.0 MB (368955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3f04d3f97aa937624b5114ac4dd0983466a2e78b211d68d50efe1d42fd169b`  
		Last Modified: Wed, 10 Jun 2020 07:31:22 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e1213818205a50e91ca9af5efcd821775b7240cc3d9c692233904104f7ab5f`  
		Last Modified: Wed, 10 Jun 2020 07:31:40 GMT  
		Size: 355.6 MB (355562058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c3fd3dcd1131659d8baa398f5d3a6376b790c597810d7b5c9342a2f3933fb4`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858a0d6d6b459adad8f2c83610893ebf6b711b4a88302ddb7084dc38168bec3`  
		Last Modified: Wed, 10 Jun 2020 07:31:21 GMT  
		Size: 986.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8fbfc68a90cc72b7f3aab6bf5671bda5ddb5f40dcda9dca22fc390b2aa7cb6`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae3529746a18c5d8522d2c6c0ada87907a2d94dff33ab693fe8f27c1d8c5b3a`  
		Last Modified: Wed, 10 Jun 2020 07:31:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
