<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sonarqube`

-	[`sonarqube:7.9.3-community`](#sonarqube793-community)
-	[`sonarqube:7.9-community`](#sonarqube79-community)
-	[`sonarqube:8.3-community`](#sonarqube83-community)
-	[`sonarqube:8.3-developer`](#sonarqube83-developer)
-	[`sonarqube:8.3-enterprise`](#sonarqube83-enterprise)
-	[`sonarqube:8-community`](#sonarqube8-community)
-	[`sonarqube:8-developer`](#sonarqube8-developer)
-	[`sonarqube:8-enterprise`](#sonarqube8-enterprise)
-	[`sonarqube:community`](#sonarqubecommunity)
-	[`sonarqube:developer`](#sonarqubedeveloper)
-	[`sonarqube:enterprise`](#sonarqubeenterprise)
-	[`sonarqube:latest`](#sonarqubelatest)
-	[`sonarqube:lts`](#sonarqubelts)

## `sonarqube:7.9.3-community`

```console
$ docker pull sonarqube@sha256:c02bfbc7d3ceb52d412aa77d7f65353dccc4265dda8e172bd59b42168ad3596e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:7.9.3-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:938289ef6dc109f0f5e7cfcfc0889fa74460fdabaf6e0295f01c61bb6eeb78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286696130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b02f27ae9f665912e7c871a13ec42a565ed765d125d4564a36dd8d2efd1fef4`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:17:54 GMT
RUN apt-get update     && apt-get install -y curl gnupg2 unzip     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:17:55 GMT
ENV SONAR_VERSION=7.9.3 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Fri, 24 Apr 2020 00:17:55 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:17:57 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:17:58 GMT
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done
# Fri, 24 Apr 2020 00:18:18 GMT
RUN set -x     && cd /opt     && curl -o sonarqube.zip -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && chown -R sonarqube:sonarqube sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Fri, 24 Apr 2020 00:18:18 GMT
VOLUME [/opt/sonarqube/data]
# Fri, 24 Apr 2020 00:18:19 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:18:19 GMT
COPY file:aa007fcc6be4125cbbb27fe345978294add03a4f05e942a5208a37be832addca in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:18:20 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:18:20 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae95c827c965c5245b284ced2d259aad6f208494cda71e13c473b5c70b08a3f6`  
		Last Modified: Fri, 24 Apr 2020 00:20:44 GMT  
		Size: 6.0 MB (5984891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26180419abe5e8e70af022476fc9a58b2b3d88872ca43d727de0d38377bf002`  
		Last Modified: Fri, 24 Apr 2020 00:20:41 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a1c9c4b364c48409066de89a9847c3eed3b28e4265c93d04fe06634f040605`  
		Last Modified: Fri, 24 Apr 2020 00:20:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449e11a96ad4b1e6dd84aa28d1d5718ce597534c2ae2e97f645fc98032d5d8da`  
		Last Modified: Fri, 24 Apr 2020 00:21:05 GMT  
		Size: 208.1 MB (208144747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c5e9243b32b7f9f0a9a61f3fe28677ce1dc232612ea49ceb14a3a3e815bcbc`  
		Last Modified: Fri, 24 Apr 2020 00:20:41 GMT  
		Size: 789.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:7.9-community`

```console
$ docker pull sonarqube@sha256:c02bfbc7d3ceb52d412aa77d7f65353dccc4265dda8e172bd59b42168ad3596e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:7.9-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:938289ef6dc109f0f5e7cfcfc0889fa74460fdabaf6e0295f01c61bb6eeb78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286696130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b02f27ae9f665912e7c871a13ec42a565ed765d125d4564a36dd8d2efd1fef4`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:17:54 GMT
RUN apt-get update     && apt-get install -y curl gnupg2 unzip     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:17:55 GMT
ENV SONAR_VERSION=7.9.3 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Fri, 24 Apr 2020 00:17:55 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:17:57 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:17:58 GMT
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done
# Fri, 24 Apr 2020 00:18:18 GMT
RUN set -x     && cd /opt     && curl -o sonarqube.zip -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && chown -R sonarqube:sonarqube sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Fri, 24 Apr 2020 00:18:18 GMT
VOLUME [/opt/sonarqube/data]
# Fri, 24 Apr 2020 00:18:19 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:18:19 GMT
COPY file:aa007fcc6be4125cbbb27fe345978294add03a4f05e942a5208a37be832addca in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:18:20 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:18:20 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae95c827c965c5245b284ced2d259aad6f208494cda71e13c473b5c70b08a3f6`  
		Last Modified: Fri, 24 Apr 2020 00:20:44 GMT  
		Size: 6.0 MB (5984891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26180419abe5e8e70af022476fc9a58b2b3d88872ca43d727de0d38377bf002`  
		Last Modified: Fri, 24 Apr 2020 00:20:41 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a1c9c4b364c48409066de89a9847c3eed3b28e4265c93d04fe06634f040605`  
		Last Modified: Fri, 24 Apr 2020 00:20:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449e11a96ad4b1e6dd84aa28d1d5718ce597534c2ae2e97f645fc98032d5d8da`  
		Last Modified: Fri, 24 Apr 2020 00:21:05 GMT  
		Size: 208.1 MB (208144747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c5e9243b32b7f9f0a9a61f3fe28677ce1dc232612ea49ceb14a3a3e815bcbc`  
		Last Modified: Fri, 24 Apr 2020 00:20:41 GMT  
		Size: 789.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.3-community`

**does not exist** (yet?)

## `sonarqube:8.3-developer`

**does not exist** (yet?)

## `sonarqube:8.3-enterprise`

**does not exist** (yet?)

## `sonarqube:8-community`

```console
$ docker pull sonarqube@sha256:a246bc64207e69bdc3919ac24d7a0526633e0d4560c66a5f7abd6ea2cc25925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:165a427f43f23c1908ef6835ab5298a006e0631068e9eb5276d56fedd859f0af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302191286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02790b4f52037e3915ef0543ddd537787514e033909719809bc475aa277cccb`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:18:43 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:18:43 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:18:45 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:18:46 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 24 Apr 2020 00:18:47 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
# Fri, 24 Apr 2020 00:18:47 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 24 Apr 2020 00:18:47 GMT
SHELL [/bin/bash -c]
# Fri, 24 Apr 2020 00:18:49 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 24 Apr 2020 00:19:09 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "$SONARQUBE_ZIP_URL"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 24 Apr 2020 00:19:10 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:19:10 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:19:11 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:19:12 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7021914086a179ca62363693d1c4ed3b0d3af0a77de2646abaec29284b12b`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 8.7 MB (8709087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe812280480d89b1a213d9874edb37a9446844b83fec4baf8dae873be0e4bd`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b35c403b0a19f5b4ece849c84d4e9e25ff9cd8522525b0f80d449707d07be33`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 15.0 KB (14986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47cc096ce369b30ac499924f7a734b30993f3404bcd891631613ebf690c9295`  
		Last Modified: Fri, 24 Apr 2020 00:21:36 GMT  
		Size: 220.9 MB (220902570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd99157f947180c9a17d06a1330cc7451206acec4b29c5517232a045754c385`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-developer`

```console
$ docker pull sonarqube@sha256:61b18120c0d974ecf92ea962b3308dad3d4da82c487ab5fda50a82efb4a0fdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:cb8ffb61c6f4d38c608fbaa9acb30a3851ae0eb6f7d35ad2cae3b3bab2ef7575
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363901367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50306df22d0910e3f914ad9b98427365954cea4030c5e0168fec78e468a38233`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:18:43 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:18:43 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:18:45 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:18:46 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 24 Apr 2020 00:19:18 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
# Fri, 24 Apr 2020 00:19:18 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 24 Apr 2020 00:19:19 GMT
SHELL [/bin/bash -c]
# Fri, 24 Apr 2020 00:19:20 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 24 Apr 2020 00:19:45 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "$SONARQUBE_ZIP_URL"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 24 Apr 2020 00:19:45 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:19:46 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:19:46 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:19:47 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7021914086a179ca62363693d1c4ed3b0d3af0a77de2646abaec29284b12b`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 8.7 MB (8709087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe812280480d89b1a213d9874edb37a9446844b83fec4baf8dae873be0e4bd`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b1380dcdc14d4ce05ad20180cf2a25c335bef3a2b5228a602f43ebf16d5e1b`  
		Last Modified: Fri, 24 Apr 2020 00:21:44 GMT  
		Size: 15.0 KB (14984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1db587c4daf86b43bdb4cda3d55ad99ea5fe1fe85e876878d0e5613650a3e9`  
		Last Modified: Fri, 24 Apr 2020 00:22:13 GMT  
		Size: 282.6 MB (282612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f356aae164a4843a89267bccc342d9d5f0744b703e40ab4bdf6cbece3318605`  
		Last Modified: Fri, 24 Apr 2020 00:21:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-enterprise`

```console
$ docker pull sonarqube@sha256:c8d3fa8de7762000eab6789adbb44a988c19ba82336439aa85d64984fdcb161f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:43eb0a861e46e435ad54421394bf3c932a274c421919c432d8022565b113bdf0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385723453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a848b722c3651c568c2028ea4917c727bb6597bbd3ae8e428fe810689d0e5d9c`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:18:43 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:18:43 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:18:45 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:18:46 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 24 Apr 2020 00:19:53 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
# Fri, 24 Apr 2020 00:19:53 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 24 Apr 2020 00:19:53 GMT
SHELL [/bin/bash -c]
# Fri, 24 Apr 2020 00:19:55 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 24 Apr 2020 00:20:20 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "${SONARQUBE_ZIP_URL}"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 24 Apr 2020 00:20:21 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:20:22 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:20:22 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:20:22 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7021914086a179ca62363693d1c4ed3b0d3af0a77de2646abaec29284b12b`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 8.7 MB (8709087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe812280480d89b1a213d9874edb37a9446844b83fec4baf8dae873be0e4bd`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c2d2ee1059102fea28d7c17b231af04d7fcb817edb4aa6ed6d36f00caf1df9`  
		Last Modified: Fri, 24 Apr 2020 00:22:19 GMT  
		Size: 15.0 KB (14986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0942ae2aaaaa6c7511ffb4dd90041949cd2cf81f331ff5c79ce7a460f0d076db`  
		Last Modified: Fri, 24 Apr 2020 00:22:49 GMT  
		Size: 304.4 MB (304434738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447de7a3791a81779bfa28404d3b72d26027aafa91ec2b53a447c8eccd8c591e`  
		Last Modified: Fri, 24 Apr 2020 00:22:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:community`

```console
$ docker pull sonarqube@sha256:a246bc64207e69bdc3919ac24d7a0526633e0d4560c66a5f7abd6ea2cc25925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:community` - linux; amd64

```console
$ docker pull sonarqube@sha256:165a427f43f23c1908ef6835ab5298a006e0631068e9eb5276d56fedd859f0af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302191286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02790b4f52037e3915ef0543ddd537787514e033909719809bc475aa277cccb`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:18:43 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:18:43 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:18:45 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:18:46 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 24 Apr 2020 00:18:47 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
# Fri, 24 Apr 2020 00:18:47 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 24 Apr 2020 00:18:47 GMT
SHELL [/bin/bash -c]
# Fri, 24 Apr 2020 00:18:49 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 24 Apr 2020 00:19:09 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "$SONARQUBE_ZIP_URL"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 24 Apr 2020 00:19:10 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:19:10 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:19:11 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:19:12 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7021914086a179ca62363693d1c4ed3b0d3af0a77de2646abaec29284b12b`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 8.7 MB (8709087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe812280480d89b1a213d9874edb37a9446844b83fec4baf8dae873be0e4bd`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b35c403b0a19f5b4ece849c84d4e9e25ff9cd8522525b0f80d449707d07be33`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 15.0 KB (14986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47cc096ce369b30ac499924f7a734b30993f3404bcd891631613ebf690c9295`  
		Last Modified: Fri, 24 Apr 2020 00:21:36 GMT  
		Size: 220.9 MB (220902570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd99157f947180c9a17d06a1330cc7451206acec4b29c5517232a045754c385`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:developer`

```console
$ docker pull sonarqube@sha256:61b18120c0d974ecf92ea962b3308dad3d4da82c487ab5fda50a82efb4a0fdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:cb8ffb61c6f4d38c608fbaa9acb30a3851ae0eb6f7d35ad2cae3b3bab2ef7575
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363901367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50306df22d0910e3f914ad9b98427365954cea4030c5e0168fec78e468a38233`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:18:43 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:18:43 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:18:45 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:18:46 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 24 Apr 2020 00:19:18 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
# Fri, 24 Apr 2020 00:19:18 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 24 Apr 2020 00:19:19 GMT
SHELL [/bin/bash -c]
# Fri, 24 Apr 2020 00:19:20 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 24 Apr 2020 00:19:45 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "$SONARQUBE_ZIP_URL"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 24 Apr 2020 00:19:45 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:19:46 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:19:46 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:19:47 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7021914086a179ca62363693d1c4ed3b0d3af0a77de2646abaec29284b12b`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 8.7 MB (8709087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe812280480d89b1a213d9874edb37a9446844b83fec4baf8dae873be0e4bd`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b1380dcdc14d4ce05ad20180cf2a25c335bef3a2b5228a602f43ebf16d5e1b`  
		Last Modified: Fri, 24 Apr 2020 00:21:44 GMT  
		Size: 15.0 KB (14984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1db587c4daf86b43bdb4cda3d55ad99ea5fe1fe85e876878d0e5613650a3e9`  
		Last Modified: Fri, 24 Apr 2020 00:22:13 GMT  
		Size: 282.6 MB (282612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f356aae164a4843a89267bccc342d9d5f0744b703e40ab4bdf6cbece3318605`  
		Last Modified: Fri, 24 Apr 2020 00:21:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:enterprise`

```console
$ docker pull sonarqube@sha256:c8d3fa8de7762000eab6789adbb44a988c19ba82336439aa85d64984fdcb161f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:43eb0a861e46e435ad54421394bf3c932a274c421919c432d8022565b113bdf0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385723453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a848b722c3651c568c2028ea4917c727bb6597bbd3ae8e428fe810689d0e5d9c`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:18:43 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:18:43 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:18:45 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:18:46 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 24 Apr 2020 00:19:53 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
# Fri, 24 Apr 2020 00:19:53 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 24 Apr 2020 00:19:53 GMT
SHELL [/bin/bash -c]
# Fri, 24 Apr 2020 00:19:55 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 24 Apr 2020 00:20:20 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "${SONARQUBE_ZIP_URL}"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 24 Apr 2020 00:20:21 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:20:22 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:20:22 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:20:22 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7021914086a179ca62363693d1c4ed3b0d3af0a77de2646abaec29284b12b`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 8.7 MB (8709087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe812280480d89b1a213d9874edb37a9446844b83fec4baf8dae873be0e4bd`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c2d2ee1059102fea28d7c17b231af04d7fcb817edb4aa6ed6d36f00caf1df9`  
		Last Modified: Fri, 24 Apr 2020 00:22:19 GMT  
		Size: 15.0 KB (14986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0942ae2aaaaa6c7511ffb4dd90041949cd2cf81f331ff5c79ce7a460f0d076db`  
		Last Modified: Fri, 24 Apr 2020 00:22:49 GMT  
		Size: 304.4 MB (304434738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447de7a3791a81779bfa28404d3b72d26027aafa91ec2b53a447c8eccd8c591e`  
		Last Modified: Fri, 24 Apr 2020 00:22:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:latest`

```console
$ docker pull sonarqube@sha256:a246bc64207e69bdc3919ac24d7a0526633e0d4560c66a5f7abd6ea2cc25925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:latest` - linux; amd64

```console
$ docker pull sonarqube@sha256:165a427f43f23c1908ef6835ab5298a006e0631068e9eb5276d56fedd859f0af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302191286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02790b4f52037e3915ef0543ddd537787514e033909719809bc475aa277cccb`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:18:43 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:18:43 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:18:45 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:18:46 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 24 Apr 2020 00:18:47 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
# Fri, 24 Apr 2020 00:18:47 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 24 Apr 2020 00:18:47 GMT
SHELL [/bin/bash -c]
# Fri, 24 Apr 2020 00:18:49 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 24 Apr 2020 00:19:09 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "$SONARQUBE_ZIP_URL"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 24 Apr 2020 00:19:10 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:19:10 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:19:11 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:19:12 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7021914086a179ca62363693d1c4ed3b0d3af0a77de2646abaec29284b12b`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 8.7 MB (8709087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe812280480d89b1a213d9874edb37a9446844b83fec4baf8dae873be0e4bd`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b35c403b0a19f5b4ece849c84d4e9e25ff9cd8522525b0f80d449707d07be33`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 15.0 KB (14986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47cc096ce369b30ac499924f7a734b30993f3404bcd891631613ebf690c9295`  
		Last Modified: Fri, 24 Apr 2020 00:21:36 GMT  
		Size: 220.9 MB (220902570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd99157f947180c9a17d06a1330cc7451206acec4b29c5517232a045754c385`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:lts`

```console
$ docker pull sonarqube@sha256:c02bfbc7d3ceb52d412aa77d7f65353dccc4265dda8e172bd59b42168ad3596e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:lts` - linux; amd64

```console
$ docker pull sonarqube@sha256:938289ef6dc109f0f5e7cfcfc0889fa74460fdabaf6e0295f01c61bb6eeb78d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286696130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b02f27ae9f665912e7c871a13ec42a565ed765d125d4564a36dd8d2efd1fef4`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:17:54 GMT
RUN apt-get update     && apt-get install -y curl gnupg2 unzip     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:17:55 GMT
ENV SONAR_VERSION=7.9.3 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Fri, 24 Apr 2020 00:17:55 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:17:57 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:17:58 GMT
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done
# Fri, 24 Apr 2020 00:18:18 GMT
RUN set -x     && cd /opt     && curl -o sonarqube.zip -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && chown -R sonarqube:sonarqube sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Fri, 24 Apr 2020 00:18:18 GMT
VOLUME [/opt/sonarqube/data]
# Fri, 24 Apr 2020 00:18:19 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:18:19 GMT
COPY file:aa007fcc6be4125cbbb27fe345978294add03a4f05e942a5208a37be832addca in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:18:20 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:18:20 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae95c827c965c5245b284ced2d259aad6f208494cda71e13c473b5c70b08a3f6`  
		Last Modified: Fri, 24 Apr 2020 00:20:44 GMT  
		Size: 6.0 MB (5984891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26180419abe5e8e70af022476fc9a58b2b3d88872ca43d727de0d38377bf002`  
		Last Modified: Fri, 24 Apr 2020 00:20:41 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a1c9c4b364c48409066de89a9847c3eed3b28e4265c93d04fe06634f040605`  
		Last Modified: Fri, 24 Apr 2020 00:20:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449e11a96ad4b1e6dd84aa28d1d5718ce597534c2ae2e97f645fc98032d5d8da`  
		Last Modified: Fri, 24 Apr 2020 00:21:05 GMT  
		Size: 208.1 MB (208144747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c5e9243b32b7f9f0a9a61f3fe28677ce1dc232612ea49ceb14a3a3e815bcbc`  
		Last Modified: Fri, 24 Apr 2020 00:20:41 GMT  
		Size: 789.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
