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
$ docker pull nuxeo@sha256:9c6121e49d6903f2476fbdac130cfa0f8d8e487164f1c1a04f806eb441271b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:10` - linux; amd64

```console
$ docker pull nuxeo@sha256:e3c6160979d3d9354e20392d3a4c8c90187cf8af18bfe9513866835dfa4550f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.2 MB (954242977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00c19d6c114a19233ddc2b79291a2812f3dcd5723ba58afe0eba57bf76d504b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:10 GMT
ARG NUXEO_VERSION=10.10
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Thu, 16 Apr 2020 01:24:12 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:38 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:38 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:38 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:39 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:39 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:40 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:40 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:40 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:40 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab4fc6238cec0d6466c0aa4ab06e8c10432a679b686306ab85bce4592b289c`  
		Last Modified: Thu, 16 Apr 2020 01:29:44 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677c0a62069c663778d5c68cada72edcdf18f1a85369754178a0e4a8f170b218`  
		Last Modified: Thu, 16 Apr 2020 01:30:35 GMT  
		Size: 355.6 MB (355562031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a945e2f4e10faeaf15c95796d53ab0f67af1d69efa345f2a88222bb014885a`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1e55871646282e7531e220468a582300b15438dc18b545c79981c0b4f4627`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec512d207b8fcf39e650c4bd06d08b97a7f804f4b90cb38829075eba2e3c48a4`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0542658e20efe0701ad72f631d7d118d7682a91bd20970242035bfbdf2b6243`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:10.10`

```console
$ docker pull nuxeo@sha256:9c6121e49d6903f2476fbdac130cfa0f8d8e487164f1c1a04f806eb441271b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:10.10` - linux; amd64

```console
$ docker pull nuxeo@sha256:e3c6160979d3d9354e20392d3a4c8c90187cf8af18bfe9513866835dfa4550f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.2 MB (954242977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00c19d6c114a19233ddc2b79291a2812f3dcd5723ba58afe0eba57bf76d504b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:10 GMT
ARG NUXEO_VERSION=10.10
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Thu, 16 Apr 2020 01:24:12 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:38 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:38 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:38 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:39 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:39 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:40 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:40 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:40 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:40 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab4fc6238cec0d6466c0aa4ab06e8c10432a679b686306ab85bce4592b289c`  
		Last Modified: Thu, 16 Apr 2020 01:29:44 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677c0a62069c663778d5c68cada72edcdf18f1a85369754178a0e4a8f170b218`  
		Last Modified: Thu, 16 Apr 2020 01:30:35 GMT  
		Size: 355.6 MB (355562031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a945e2f4e10faeaf15c95796d53ab0f67af1d69efa345f2a88222bb014885a`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1e55871646282e7531e220468a582300b15438dc18b545c79981c0b4f4627`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec512d207b8fcf39e650c4bd06d08b97a7f804f4b90cb38829075eba2e3c48a4`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0542658e20efe0701ad72f631d7d118d7682a91bd20970242035bfbdf2b6243`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:7`

```console
$ docker pull nuxeo@sha256:03cc2f3c671ca43721d3c93bb8d5e1068f6c28b91a81cc6e8c58838aacabcaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:7` - linux; amd64

```console
$ docker pull nuxeo@sha256:6d3c4440ff8c6c85fa88ba7012cb2665cd0be085eddee431507f76f68a75342a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1155547468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb022c455c95a5732014c95b79cf110609379d97785f3fa3dd86ec7fa476b56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libreoffice     libwpd-tools     exiftool     ghostscript  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:21:00 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:21:01 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:21:01 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:01 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_VERSION=7.10
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2
# Thu, 16 Apr 2020 01:21:02 GMT
ENV LAUNCHER_DEBUG=-Djvmcheck=nofail
# Thu, 16 Apr 2020 01:21:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:21:23 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh
# Thu, 16 Apr 2020 01:21:34 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:21:35 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:21:35 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:21:36 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:36 GMT
COPY file:9560db752e0d728d2bb67749bc399b34de55ac127e1fda9bab6523a33ac2fd8c in / 
# Thu, 16 Apr 2020 01:21:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:21:36 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:21:36 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:21:37 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4e7a4cfe89faf9fc2ea68685e5110960fb2a33195a75f9e67f7e19773c9d4b`  
		Last Modified: Thu, 16 Apr 2020 01:26:05 GMT  
		Size: 364.9 MB (364915473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3274a27bdb50beb86a2f2eb3d3f2ffbbedf1cb897dd9efab60ce595bdb133c7a`  
		Last Modified: Thu, 16 Apr 2020 01:24:52 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfa78a1fdd050032664ece080a28f766186672751207b2e0a65d102126b39e8`  
		Last Modified: Thu, 16 Apr 2020 01:25:39 GMT  
		Size: 280.5 MB (280457932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca908561fc15cbef1497e1882e8472c5e139f2b793df9558365d679662b1a105`  
		Last Modified: Thu, 16 Apr 2020 01:26:52 GMT  
		Size: 280.5 MB (280459878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51fa4751275d62e6d0f433775209f0aa6202244b3a0855a0a64703735f29498`  
		Last Modified: Thu, 16 Apr 2020 01:24:51 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e39b9c3a6f3b21f9837c7cda28fd0aad9b5e3e01d9d036f4d6cc877b4b468e`  
		Last Modified: Thu, 16 Apr 2020 01:24:52 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:7.10`

```console
$ docker pull nuxeo@sha256:03cc2f3c671ca43721d3c93bb8d5e1068f6c28b91a81cc6e8c58838aacabcaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:7.10` - linux; amd64

```console
$ docker pull nuxeo@sha256:6d3c4440ff8c6c85fa88ba7012cb2665cd0be085eddee431507f76f68a75342a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1155547468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb022c455c95a5732014c95b79cf110609379d97785f3fa3dd86ec7fa476b56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libreoffice     libwpd-tools     exiftool     ghostscript  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:21:00 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:21:01 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:21:01 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:01 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_VERSION=7.10
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2
# Thu, 16 Apr 2020 01:21:02 GMT
ENV LAUNCHER_DEBUG=-Djvmcheck=nofail
# Thu, 16 Apr 2020 01:21:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:21:23 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh
# Thu, 16 Apr 2020 01:21:34 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:21:35 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:21:35 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:21:36 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:36 GMT
COPY file:9560db752e0d728d2bb67749bc399b34de55ac127e1fda9bab6523a33ac2fd8c in / 
# Thu, 16 Apr 2020 01:21:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:21:36 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:21:36 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:21:37 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4e7a4cfe89faf9fc2ea68685e5110960fb2a33195a75f9e67f7e19773c9d4b`  
		Last Modified: Thu, 16 Apr 2020 01:26:05 GMT  
		Size: 364.9 MB (364915473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3274a27bdb50beb86a2f2eb3d3f2ffbbedf1cb897dd9efab60ce595bdb133c7a`  
		Last Modified: Thu, 16 Apr 2020 01:24:52 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfa78a1fdd050032664ece080a28f766186672751207b2e0a65d102126b39e8`  
		Last Modified: Thu, 16 Apr 2020 01:25:39 GMT  
		Size: 280.5 MB (280457932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca908561fc15cbef1497e1882e8472c5e139f2b793df9558365d679662b1a105`  
		Last Modified: Thu, 16 Apr 2020 01:26:52 GMT  
		Size: 280.5 MB (280459878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51fa4751275d62e6d0f433775209f0aa6202244b3a0855a0a64703735f29498`  
		Last Modified: Thu, 16 Apr 2020 01:24:51 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e39b9c3a6f3b21f9837c7cda28fd0aad9b5e3e01d9d036f4d6cc877b4b468e`  
		Last Modified: Thu, 16 Apr 2020 01:24:52 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:8`

```console
$ docker pull nuxeo@sha256:8a64ca3a917665914321f3a488a7338eee2d3dc9a13a6df17f535805f9830779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:8` - linux; amd64

```console
$ docker pull nuxeo@sha256:9e0f823013ab5f446616a2003bfb1d8c5fe03c1c63047e1cee9e96048bbab6b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.3 MB (868303663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497dde762ed30a065bf771aea6f241debb2f5da046448c2655528b1fc791fcce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_VERSION=8.10
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_MD5=29e67a19bba54099093b51d892926be1
# Thu, 16 Apr 2020 01:23:06 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:23:25 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:23:29 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:23:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:23:29 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:30 GMT
COPY file:bb9febfdc3a76dbd4a80d559b47951e49fca7137ad3b76ce7b7293512f63b257 in / 
# Thu, 16 Apr 2020 01:23:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:23:30 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:23:30 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:23:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250fe8ebb4f9a212587efd5a08a8758ca28bad0a0227981ad85d10b0e8294be`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bc027495fe50def0cb89e6e2cd9982a3884043e7ca61177caa46dc5e1551ef`  
		Last Modified: Thu, 16 Apr 2020 01:27:30 GMT  
		Size: 269.6 MB (269624437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1c5b413f2bbda8e5a99134ff1e9b91c48d281dff0909a5e3259143ea13938c`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 785.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08790c230cf7c26cdaa75855bfffc74950d2ee1808d3c721b2f680749baba1`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:8.10`

```console
$ docker pull nuxeo@sha256:8a64ca3a917665914321f3a488a7338eee2d3dc9a13a6df17f535805f9830779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:8.10` - linux; amd64

```console
$ docker pull nuxeo@sha256:9e0f823013ab5f446616a2003bfb1d8c5fe03c1c63047e1cee9e96048bbab6b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.3 MB (868303663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497dde762ed30a065bf771aea6f241debb2f5da046448c2655528b1fc791fcce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_VERSION=8.10
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_MD5=29e67a19bba54099093b51d892926be1
# Thu, 16 Apr 2020 01:23:06 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:23:25 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:23:29 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:23:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:23:29 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:30 GMT
COPY file:bb9febfdc3a76dbd4a80d559b47951e49fca7137ad3b76ce7b7293512f63b257 in / 
# Thu, 16 Apr 2020 01:23:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:23:30 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:23:30 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:23:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250fe8ebb4f9a212587efd5a08a8758ca28bad0a0227981ad85d10b0e8294be`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bc027495fe50def0cb89e6e2cd9982a3884043e7ca61177caa46dc5e1551ef`  
		Last Modified: Thu, 16 Apr 2020 01:27:30 GMT  
		Size: 269.6 MB (269624437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1c5b413f2bbda8e5a99134ff1e9b91c48d281dff0909a5e3259143ea13938c`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 785.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08790c230cf7c26cdaa75855bfffc74950d2ee1808d3c721b2f680749baba1`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:9`

```console
$ docker pull nuxeo@sha256:fa3d484ead1d0a225f6de3a0e0f213434c72e0c682ebffb93487ebb07b86cb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:9` - linux; amd64

```console
$ docker pull nuxeo@sha256:a07b5e021bcdf25c539918fde02613b0906b05944e96a6518ad5b277f311755d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.8 MB (983837375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5023933eb41ad342d5436863760c8a00299d1dc0448b59ec2493a69539133314`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_VERSION=9.10
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_MD5=327d23bbd5558565694027b11c0dd82a
# Thu, 16 Apr 2020 01:23:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:04 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:04 GMT
COPY dir:1d4b19e1e35500d85eafcc58364498b9325f119ce19917cefc60c7ad98e600e7 in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:04 GMT
COPY file:8f1eb15b3cc87be8784ed6bc39c958a3a06d1e375bda2ce728f297d14d74d526 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:04 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:05 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:05 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:05 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:06 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:06 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:06 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:06 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c041408f40bc290f1dd5b3e41abb30792682da7fc2fc3ce5b193352b6b780c7`  
		Last Modified: Thu, 16 Apr 2020 01:28:53 GMT  
		Size: 4.4 KB (4379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03724c41c81cd669811372466819a039a2f2b6bced727b4717128b29975e7ce`  
		Last Modified: Thu, 16 Apr 2020 01:29:38 GMT  
		Size: 385.2 MB (385156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1a0972c3d18c5f6f55acfc9710264fe5b17ab43a2bf375dff4774268a93f57`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0638ab26dcd104d125180257c5661fe8082d3d9cec5bdfd2b1362a333f4a89`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014f531d6d84ab4cc5248665d6b65a67a504661916c8d41c3650624ca806a6ae`  
		Last Modified: Thu, 16 Apr 2020 01:28:53 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27057c1f208502a5d6d089785a069f4856436c8e604124f41c2f67e4b385afca`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:9.10`

```console
$ docker pull nuxeo@sha256:fa3d484ead1d0a225f6de3a0e0f213434c72e0c682ebffb93487ebb07b86cb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:9.10` - linux; amd64

```console
$ docker pull nuxeo@sha256:a07b5e021bcdf25c539918fde02613b0906b05944e96a6518ad5b277f311755d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.8 MB (983837375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5023933eb41ad342d5436863760c8a00299d1dc0448b59ec2493a69539133314`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_VERSION=9.10
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_MD5=327d23bbd5558565694027b11c0dd82a
# Thu, 16 Apr 2020 01:23:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:04 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:04 GMT
COPY dir:1d4b19e1e35500d85eafcc58364498b9325f119ce19917cefc60c7ad98e600e7 in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:04 GMT
COPY file:8f1eb15b3cc87be8784ed6bc39c958a3a06d1e375bda2ce728f297d14d74d526 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:04 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:05 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:05 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:05 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:06 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:06 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:06 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:06 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c041408f40bc290f1dd5b3e41abb30792682da7fc2fc3ce5b193352b6b780c7`  
		Last Modified: Thu, 16 Apr 2020 01:28:53 GMT  
		Size: 4.4 KB (4379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03724c41c81cd669811372466819a039a2f2b6bced727b4717128b29975e7ce`  
		Last Modified: Thu, 16 Apr 2020 01:29:38 GMT  
		Size: 385.2 MB (385156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1a0972c3d18c5f6f55acfc9710264fe5b17ab43a2bf375dff4774268a93f57`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0638ab26dcd104d125180257c5661fe8082d3d9cec5bdfd2b1362a333f4a89`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014f531d6d84ab4cc5248665d6b65a67a504661916c8d41c3650624ca806a6ae`  
		Last Modified: Thu, 16 Apr 2020 01:28:53 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27057c1f208502a5d6d089785a069f4856436c8e604124f41c2f67e4b385afca`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:FT`

```console
$ docker pull nuxeo@sha256:9c6121e49d6903f2476fbdac130cfa0f8d8e487164f1c1a04f806eb441271b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:FT` - linux; amd64

```console
$ docker pull nuxeo@sha256:e3c6160979d3d9354e20392d3a4c8c90187cf8af18bfe9513866835dfa4550f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.2 MB (954242977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00c19d6c114a19233ddc2b79291a2812f3dcd5723ba58afe0eba57bf76d504b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:10 GMT
ARG NUXEO_VERSION=10.10
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Thu, 16 Apr 2020 01:24:12 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:38 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:38 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:38 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:39 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:39 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:40 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:40 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:40 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:40 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab4fc6238cec0d6466c0aa4ab06e8c10432a679b686306ab85bce4592b289c`  
		Last Modified: Thu, 16 Apr 2020 01:29:44 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677c0a62069c663778d5c68cada72edcdf18f1a85369754178a0e4a8f170b218`  
		Last Modified: Thu, 16 Apr 2020 01:30:35 GMT  
		Size: 355.6 MB (355562031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a945e2f4e10faeaf15c95796d53ab0f67af1d69efa345f2a88222bb014885a`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1e55871646282e7531e220468a582300b15438dc18b545c79981c0b4f4627`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec512d207b8fcf39e650c4bd06d08b97a7f804f4b90cb38829075eba2e3c48a4`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0542658e20efe0701ad72f631d7d118d7682a91bd20970242035bfbdf2b6243`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:latest`

```console
$ docker pull nuxeo@sha256:9c6121e49d6903f2476fbdac130cfa0f8d8e487164f1c1a04f806eb441271b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:latest` - linux; amd64

```console
$ docker pull nuxeo@sha256:e3c6160979d3d9354e20392d3a4c8c90187cf8af18bfe9513866835dfa4550f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.2 MB (954242977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00c19d6c114a19233ddc2b79291a2812f3dcd5723ba58afe0eba57bf76d504b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:10 GMT
ARG NUXEO_VERSION=10.10
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Thu, 16 Apr 2020 01:24:12 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:38 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:38 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:38 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:39 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:39 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:40 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:40 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:40 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:40 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab4fc6238cec0d6466c0aa4ab06e8c10432a679b686306ab85bce4592b289c`  
		Last Modified: Thu, 16 Apr 2020 01:29:44 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677c0a62069c663778d5c68cada72edcdf18f1a85369754178a0e4a8f170b218`  
		Last Modified: Thu, 16 Apr 2020 01:30:35 GMT  
		Size: 355.6 MB (355562031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a945e2f4e10faeaf15c95796d53ab0f67af1d69efa345f2a88222bb014885a`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1e55871646282e7531e220468a582300b15438dc18b545c79981c0b4f4627`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec512d207b8fcf39e650c4bd06d08b97a7f804f4b90cb38829075eba2e3c48a4`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0542658e20efe0701ad72f631d7d118d7682a91bd20970242035bfbdf2b6243`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS`

```console
$ docker pull nuxeo@sha256:9c6121e49d6903f2476fbdac130cfa0f8d8e487164f1c1a04f806eb441271b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS` - linux; amd64

```console
$ docker pull nuxeo@sha256:e3c6160979d3d9354e20392d3a4c8c90187cf8af18bfe9513866835dfa4550f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.2 MB (954242977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00c19d6c114a19233ddc2b79291a2812f3dcd5723ba58afe0eba57bf76d504b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:10 GMT
ARG NUXEO_VERSION=10.10
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Thu, 16 Apr 2020 01:24:12 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:38 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:38 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:38 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:39 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:39 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:40 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:40 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:40 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:40 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab4fc6238cec0d6466c0aa4ab06e8c10432a679b686306ab85bce4592b289c`  
		Last Modified: Thu, 16 Apr 2020 01:29:44 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677c0a62069c663778d5c68cada72edcdf18f1a85369754178a0e4a8f170b218`  
		Last Modified: Thu, 16 Apr 2020 01:30:35 GMT  
		Size: 355.6 MB (355562031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a945e2f4e10faeaf15c95796d53ab0f67af1d69efa345f2a88222bb014885a`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1e55871646282e7531e220468a582300b15438dc18b545c79981c0b4f4627`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec512d207b8fcf39e650c4bd06d08b97a7f804f4b90cb38829075eba2e3c48a4`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0542658e20efe0701ad72f631d7d118d7682a91bd20970242035bfbdf2b6243`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS-2015`

```console
$ docker pull nuxeo@sha256:03cc2f3c671ca43721d3c93bb8d5e1068f6c28b91a81cc6e8c58838aacabcaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS-2015` - linux; amd64

```console
$ docker pull nuxeo@sha256:6d3c4440ff8c6c85fa88ba7012cb2665cd0be085eddee431507f76f68a75342a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1155547468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb022c455c95a5732014c95b79cf110609379d97785f3fa3dd86ec7fa476b56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libreoffice     libwpd-tools     exiftool     ghostscript  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:21:00 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:21:01 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:21:01 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:01 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_VERSION=7.10
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip
# Thu, 16 Apr 2020 01:21:01 GMT
ARG NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2
# Thu, 16 Apr 2020 01:21:02 GMT
ENV LAUNCHER_DEBUG=-Djvmcheck=nofail
# Thu, 16 Apr 2020 01:21:02 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:21:23 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh
# Thu, 16 Apr 2020 01:21:34 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:21:35 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-7.10/nuxeo-cap-7.10-tomcat.zip NUXEO_MD5=de2084b1a6fab4b1c8fb769903b044f2 NUXEO_VERSION=7.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:21:35 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:21:36 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:21:36 GMT
COPY file:9560db752e0d728d2bb67749bc399b34de55ac127e1fda9bab6523a33ac2fd8c in / 
# Thu, 16 Apr 2020 01:21:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:21:36 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:21:36 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:21:37 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4e7a4cfe89faf9fc2ea68685e5110960fb2a33195a75f9e67f7e19773c9d4b`  
		Last Modified: Thu, 16 Apr 2020 01:26:05 GMT  
		Size: 364.9 MB (364915473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3274a27bdb50beb86a2f2eb3d3f2ffbbedf1cb897dd9efab60ce595bdb133c7a`  
		Last Modified: Thu, 16 Apr 2020 01:24:52 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfa78a1fdd050032664ece080a28f766186672751207b2e0a65d102126b39e8`  
		Last Modified: Thu, 16 Apr 2020 01:25:39 GMT  
		Size: 280.5 MB (280457932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca908561fc15cbef1497e1882e8472c5e139f2b793df9558365d679662b1a105`  
		Last Modified: Thu, 16 Apr 2020 01:26:52 GMT  
		Size: 280.5 MB (280459878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51fa4751275d62e6d0f433775209f0aa6202244b3a0855a0a64703735f29498`  
		Last Modified: Thu, 16 Apr 2020 01:24:51 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e39b9c3a6f3b21f9837c7cda28fd0aad9b5e3e01d9d036f4d6cc877b4b468e`  
		Last Modified: Thu, 16 Apr 2020 01:24:52 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS-2016`

```console
$ docker pull nuxeo@sha256:8a64ca3a917665914321f3a488a7338eee2d3dc9a13a6df17f535805f9830779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS-2016` - linux; amd64

```console
$ docker pull nuxeo@sha256:9e0f823013ab5f446616a2003bfb1d8c5fe03c1c63047e1cee9e96048bbab6b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.3 MB (868303663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497dde762ed30a065bf771aea6f241debb2f5da046448c2655528b1fc791fcce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_VERSION=8.10
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip
# Thu, 16 Apr 2020 01:23:05 GMT
ARG NUXEO_MD5=29e67a19bba54099093b51d892926be1
# Thu, 16 Apr 2020 01:23:06 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:23:25 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:23:29 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-8.10/nuxeo-server-8.10-tomcat.zip NUXEO_MD5=29e67a19bba54099093b51d892926be1 NUXEO_VERSION=8.10
RUN mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d     && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:23:29 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:23:29 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:30 GMT
COPY file:bb9febfdc3a76dbd4a80d559b47951e49fca7137ad3b76ce7b7293512f63b257 in / 
# Thu, 16 Apr 2020 01:23:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:23:30 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:23:30 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:23:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250fe8ebb4f9a212587efd5a08a8758ca28bad0a0227981ad85d10b0e8294be`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bc027495fe50def0cb89e6e2cd9982a3884043e7ca61177caa46dc5e1551ef`  
		Last Modified: Thu, 16 Apr 2020 01:27:30 GMT  
		Size: 269.6 MB (269624437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1c5b413f2bbda8e5a99134ff1e9b91c48d281dff0909a5e3259143ea13938c`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 785.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08790c230cf7c26cdaa75855bfffc74950d2ee1808d3c721b2f680749baba1`  
		Last Modified: Thu, 16 Apr 2020 01:26:58 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS-2017`

```console
$ docker pull nuxeo@sha256:fa3d484ead1d0a225f6de3a0e0f213434c72e0c682ebffb93487ebb07b86cb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS-2017` - linux; amd64

```console
$ docker pull nuxeo@sha256:a07b5e021bcdf25c539918fde02613b0906b05944e96a6518ad5b277f311755d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.8 MB (983837375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5023933eb41ad342d5436863760c8a00299d1dc0448b59ec2493a69539133314`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_VERSION=9.10
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip
# Thu, 16 Apr 2020 01:23:37 GMT
ARG NUXEO_MD5=327d23bbd5558565694027b11c0dd82a
# Thu, 16 Apr 2020 01:23:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:04 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:04 GMT
COPY dir:1d4b19e1e35500d85eafcc58364498b9325f119ce19917cefc60c7ad98e600e7 in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:04 GMT
COPY file:8f1eb15b3cc87be8784ed6bc39c958a3a06d1e375bda2ce728f297d14d74d526 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:04 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:05 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.10/nuxeo-server-9.10-tomcat.zip NUXEO_MD5=327d23bbd5558565694027b11c0dd82a NUXEO_VERSION=9.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:05 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:05 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:06 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:06 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:06 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:06 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c041408f40bc290f1dd5b3e41abb30792682da7fc2fc3ce5b193352b6b780c7`  
		Last Modified: Thu, 16 Apr 2020 01:28:53 GMT  
		Size: 4.4 KB (4379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03724c41c81cd669811372466819a039a2f2b6bced727b4717128b29975e7ce`  
		Last Modified: Thu, 16 Apr 2020 01:29:38 GMT  
		Size: 385.2 MB (385156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1a0972c3d18c5f6f55acfc9710264fe5b17ab43a2bf375dff4774268a93f57`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0638ab26dcd104d125180257c5661fe8082d3d9cec5bdfd2b1362a333f4a89`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014f531d6d84ab4cc5248665d6b65a67a504661916c8d41c3650624ca806a6ae`  
		Last Modified: Thu, 16 Apr 2020 01:28:53 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27057c1f208502a5d6d089785a069f4856436c8e604124f41c2f67e4b385afca`  
		Last Modified: Thu, 16 Apr 2020 01:28:52 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nuxeo:LTS-2019`

```console
$ docker pull nuxeo@sha256:9c6121e49d6903f2476fbdac130cfa0f8d8e487164f1c1a04f806eb441271b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:LTS-2019` - linux; amd64

```console
$ docker pull nuxeo@sha256:e3c6160979d3d9354e20392d3a4c8c90187cf8af18bfe9513866835dfa4550f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.2 MB (954242977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00c19d6c114a19233ddc2b79291a2812f3dcd5723ba58afe0eba57bf76d504b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:33:40 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 00:29:28 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 00:29:35 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 16 Apr 2020 01:19:39 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 16 Apr 2020 01:23:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice     ffmpeg     x264  && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:23:04 GMT
RUN find / -perm 6000 -type f -exec chmod a-s {} \; || true
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_USER=nuxeo
# Thu, 16 Apr 2020 01:23:04 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:23:05 GMT
ENV HOME=/opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:10 GMT
ARG NUXEO_VERSION=10.10
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip
# Thu, 16 Apr 2020 01:24:11 GMT
ARG NUXEO_MD5=90ef2ac005020e880b6277510800c30c
# Thu, 16 Apr 2020 01:24:12 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 16 Apr 2020 01:24:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init     && chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME
# Thu, 16 Apr 2020 01:24:38 GMT
COPY dir:d28c2b4bdf31f5817cba5496caa3161d743da596ec68186e0c444ede39dd58ac in /opt/nuxeo/server/templates/docker 
# Thu, 16 Apr 2020 01:24:38 GMT
COPY file:dbaa7cc62ad81fbafea7350f8e1ec2045fdc4a962bcfd145d777fefaf7205910 in /etc/nuxeo/nuxeo.conf.template 
# Thu, 16 Apr 2020 01:24:38 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 16 Apr 2020 01:24:39 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-10.10/nuxeo-server-10.10-tomcat.zip NUXEO_MD5=90ef2ac005020e880b6277510800c30c NUXEO_VERSION=10.10
RUN chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d      && chmod g=u /etc/passwd
# Thu, 16 Apr 2020 01:24:39 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 01:24:40 GMT
WORKDIR /opt/nuxeo/server
# Thu, 16 Apr 2020 01:24:40 GMT
COPY file:97cc30e1ff0452e9f8e463882c4544e2dc446201ab67f037426aee9cbd1e212a in / 
# Thu, 16 Apr 2020 01:24:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:24:40 GMT
EXPOSE 8080
# Thu, 16 Apr 2020 01:24:40 GMT
CMD ["nuxeoctl" "console"]
# Thu, 16 Apr 2020 01:24:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c11ae3efe806bf739f69b5ff7592d353b64c422d5b029aa3131551019f1608`  
		Last Modified: Tue, 31 Mar 2020 21:36:39 GMT  
		Size: 5.3 MB (5284627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e595a3ef542ad0784ed4239a4add4da471a3d9a7669f723ae7eb23092b226`  
		Last Modified: Tue, 31 Mar 2020 21:37:35 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c4376876069dba34d52273a4a7b5a3f9a0fb5778b6fa1c5df6c39ee69c4`  
		Last Modified: Thu, 16 Apr 2020 00:33:12 GMT  
		Size: 104.4 MB (104441830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18022d1e8efa792c44a89290c84d9ff4b6908b967150731f70fe5ce5351e931`  
		Last Modified: Thu, 16 Apr 2020 01:28:29 GMT  
		Size: 369.0 MB (368965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab4fc6238cec0d6466c0aa4ab06e8c10432a679b686306ab85bce4592b289c`  
		Last Modified: Thu, 16 Apr 2020 01:29:44 GMT  
		Size: 4.4 KB (4377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677c0a62069c663778d5c68cada72edcdf18f1a85369754178a0e4a8f170b218`  
		Last Modified: Thu, 16 Apr 2020 01:30:35 GMT  
		Size: 355.6 MB (355562031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a945e2f4e10faeaf15c95796d53ab0f67af1d69efa345f2a88222bb014885a`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1e55871646282e7531e220468a582300b15438dc18b545c79981c0b4f4627`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec512d207b8fcf39e650c4bd06d08b97a7f804f4b90cb38829075eba2e3c48a4`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0542658e20efe0701ad72f631d7d118d7682a91bd20970242035bfbdf2b6243`  
		Last Modified: Thu, 16 Apr 2020 01:29:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
