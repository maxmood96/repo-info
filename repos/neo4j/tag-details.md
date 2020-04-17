<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:3.4`](#neo4j34)
-	[`neo4j:3.4.14`](#neo4j3414)
-	[`neo4j:3.4.14-enterprise`](#neo4j3414-enterprise)
-	[`neo4j:3.4.15`](#neo4j3415)
-	[`neo4j:3.4.15-enterprise`](#neo4j3415-enterprise)
-	[`neo4j:3.4.16`](#neo4j3416)
-	[`neo4j:3.4.16-enterprise`](#neo4j3416-enterprise)
-	[`neo4j:3.4.17`](#neo4j3417)
-	[`neo4j:3.4.17-enterprise`](#neo4j3417-enterprise)
-	[`neo4j:3.4-enterprise`](#neo4j34-enterprise)
-	[`neo4j:3.5`](#neo4j35)
-	[`neo4j:3.5.11`](#neo4j3511)
-	[`neo4j:3.5.11-enterprise`](#neo4j3511-enterprise)
-	[`neo4j:3.5.12`](#neo4j3512)
-	[`neo4j:3.5.12-enterprise`](#neo4j3512-enterprise)
-	[`neo4j:3.5.13`](#neo4j3513)
-	[`neo4j:3.5.13-enterprise`](#neo4j3513-enterprise)
-	[`neo4j:3.5.14`](#neo4j3514)
-	[`neo4j:3.5.14-enterprise`](#neo4j3514-enterprise)
-	[`neo4j:3.5.15`](#neo4j3515)
-	[`neo4j:3.5.15-enterprise`](#neo4j3515-enterprise)
-	[`neo4j:3.5.16`](#neo4j3516)
-	[`neo4j:3.5.16-enterprise`](#neo4j3516-enterprise)
-	[`neo4j:3.5.17`](#neo4j3517)
-	[`neo4j:3.5.17-enterprise`](#neo4j3517-enterprise)
-	[`neo4j:3.5.6`](#neo4j356)
-	[`neo4j:3.5.6-enterprise`](#neo4j356-enterprise)
-	[`neo4j:3.5.7`](#neo4j357)
-	[`neo4j:3.5.7-enterprise`](#neo4j357-enterprise)
-	[`neo4j:3.5.8`](#neo4j358)
-	[`neo4j:3.5.8-enterprise`](#neo4j358-enterprise)
-	[`neo4j:3.5-enterprise`](#neo4j35-enterprise)
-	[`neo4j:4.0`](#neo4j40)
-	[`neo4j:4.0.0`](#neo4j400)
-	[`neo4j:4.0.0-enterprise`](#neo4j400-enterprise)
-	[`neo4j:4.0.1`](#neo4j401)
-	[`neo4j:4.0.1-enterprise`](#neo4j401-enterprise)
-	[`neo4j:4.0.2`](#neo4j402)
-	[`neo4j:4.0.2-enterprise`](#neo4j402-enterprise)
-	[`neo4j:4.0.3`](#neo4j403)
-	[`neo4j:4.0.3-enterprise`](#neo4j403-enterprise)
-	[`neo4j:4.0-enterprise`](#neo4j40-enterprise)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:3.4`

```console
$ docker pull neo4j@sha256:f231661818c47c3f9cbbad33ab4000d144dc4697bf7f6ad9db35ff845ee97f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4` - linux; amd64

```console
$ docker pull neo4j@sha256:af91be2aa9869f48b59b0ef2118a536c201e3c9aef23e5da3f4611d62d4881a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215029509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d9ebb1497baaebf7b454ce11ca585e535a02a17f854ab8736f93a9af412033`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:47:03 GMT
ENV NEO4J_SHA256=fbb03e85a09e1e8a77c496ad61e8094ef94185268098634a4aaf1d1a01b841a6 NEO4J_TARBALL=neo4j-community-3.4.17-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:47:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
# Fri, 17 Apr 2020 10:47:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:47:04 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:47:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:47:19 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:47:19 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:47:19 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:47:19 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:47:19 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:47:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b73a9e13152369d2a8d23cbbd48b68a43f9f4f4b947d37972d89698082c867`  
		Last Modified: Fri, 17 Apr 2020 11:04:05 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7caf4345bc78392116bd6f04a8ca7c35474d93b48e32aff09cdf0e9a90d7cecd`  
		Last Modified: Fri, 17 Apr 2020 11:04:05 GMT  
		Size: 303.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b76a20cc81b87ff0ac245aaa6ce6ccff43d0e9bb65c4c2d92c852585186c2f2`  
		Last Modified: Fri, 17 Apr 2020 11:04:30 GMT  
		Size: 144.1 MB (144082226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871e8789435b28b1ddee002e20939bcc9476d4fdf1bdfd02edddb924d96c825b`  
		Last Modified: Fri, 17 Apr 2020 11:04:05 GMT  
		Size: 5.3 KB (5302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.14`

```console
$ docker pull neo4j@sha256:e4e27aac2ee0ce92ebc5cf5674ec384784eab539e8e1ebfed8aa6a8d4b63e11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.14` - linux; amd64

```console
$ docker pull neo4j@sha256:f559502ef4a513df05d58ee48964b79fecd69bcbf76a9523bc7d057c9bc9aae8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225554408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7c27501f747954ba6499ecb7774d3d688ac274269ff7bdb7826ef11490e6a2`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:49:52 GMT
ENV NEO4J_SHA256=fcbdd7abc28a50cca76daed96d60a6d7d03a4db5bbbfdfb8e520ee1984698461 NEO4J_TARBALL=neo4j-community-3.4.14-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:49:52 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.14-unix.tar.gz
# Fri, 17 Apr 2020 10:49:54 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.14-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:49:54 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:50:12 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.14-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 17 Apr 2020 10:50:13 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:50:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:50:14 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:50:15 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:50:15 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:50:15 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:50:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f42aee550b1b01e183bb0916bbc3cc63fc2a3180ac578332d3b0ca641cd8d2`  
		Last Modified: Fri, 17 Apr 2020 11:07:04 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74173bfc30da8b191ca055ec24a8215a188286a03d675a5be447ce7f445a730a`  
		Last Modified: Fri, 17 Apr 2020 11:07:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fee4d816863fa78180797b61a1f472d1de5813b6d567211a6b12cd03053c968`  
		Last Modified: Fri, 17 Apr 2020 11:07:37 GMT  
		Size: 154.6 MB (154608214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0572c18fb337a5f13ec139b700672663934a330dd039c785893c34791383065`  
		Last Modified: Fri, 17 Apr 2020 11:07:04 GMT  
		Size: 4.4 KB (4387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.14-enterprise`

```console
$ docker pull neo4j@sha256:4941ada5df7d41090d76c64aa380e42f36495eb2bd861ac5f26455dd526a4bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.14-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:31cea2991e2a01989764530496546e2ba4a97e1bf8a901f1425cb772f20216d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242334819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc2dcd3757523e27f17fad61e4db1eba186f908090737cea0d73e04b6d322a1`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:50:21 GMT
ENV NEO4J_SHA256=5ebd47769a7aa25343d0b1ea59c2e9f2c847c56ac344ce2644d1f60496a7386f NEO4J_TARBALL=neo4j-enterprise-3.4.14-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:50:22 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.14-unix.tar.gz
# Fri, 17 Apr 2020 10:50:23 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.14-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:50:24 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:50:42 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.14-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 17 Apr 2020 10:50:43 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:50:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:50:43 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:50:44 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:50:44 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:50:44 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:50:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0b4f0aa045a7e79b36472aa8fafeda5582d5628f03247c3d7687cf49471d23`  
		Last Modified: Fri, 17 Apr 2020 11:07:42 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2bdc92c499cf7c55fb1a7c757d49ca9e81c4bbefefb3e48bc5e3e3a17edc60`  
		Last Modified: Fri, 17 Apr 2020 11:07:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a5d910dc74e475659b758b8401abf45817781afd3bb759eac6989053e3564d`  
		Last Modified: Fri, 17 Apr 2020 11:08:01 GMT  
		Size: 171.4 MB (171388625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae9b6d2295bcf955ce7b86d869b61e36e494e988ee760850e6ce3997b601210`  
		Last Modified: Fri, 17 Apr 2020 11:07:42 GMT  
		Size: 4.4 KB (4386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.15`

```console
$ docker pull neo4j@sha256:92c64e5b9b4db5d7a6aa365fcfae96133ea28ec2e186e04e785916641c09f826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.15` - linux; amd64

```console
$ docker pull neo4j@sha256:9224992562a655fecf2c0cd34383cfee65cb80d5e50c5d921feb8c26613b01af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212165136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a37c0b1f1c763bdb26fcb7f62452546bbffbeb564aaed03ff451c22c192e29`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:48:52 GMT
ENV NEO4J_SHA256=7e230753e2c53c912829f1ed2df963fbacc3892acd3501a84892118317fbccda NEO4J_TARBALL=neo4j-community-3.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:48:53 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.15-unix.tar.gz
# Fri, 17 Apr 2020 10:48:55 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.15-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:48:55 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:49:13 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:49:13 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:49:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:49:13 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:49:14 GMT
COPY file:e07128b8290e38440521f56bbf78b61bbce8be21a97b8b31668594bebdd2bf2b in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:49:14 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:49:14 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:49:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a57b3a7abc3f364b59447aabe12bfffb12fe0fd99b0c277f5e9231fcb2a0e4`  
		Last Modified: Fri, 17 Apr 2020 11:06:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf498e0015cd149949eec1185e03b21d4e12e6faa9be6d2f22dba91a2d8498b4`  
		Last Modified: Fri, 17 Apr 2020 11:06:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d90ab59366b954bf79fedeea5597769cef22363b4e5598aa5ad5ef96f38fa2e`  
		Last Modified: Fri, 17 Apr 2020 11:06:40 GMT  
		Size: 141.2 MB (141218979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce2bd54e9031dd94dc97849442898d6f9dab460f39c261607f2632219ed82e`  
		Last Modified: Fri, 17 Apr 2020 11:06:09 GMT  
		Size: 4.3 KB (4348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.15-enterprise`

```console
$ docker pull neo4j@sha256:01069433433d6c939e161237f1f2a946f86075e67eea34ee8746563e40df20c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e3ef56fadb85c6912c83529518b7bdc2ccab73c959e984796a08df028477b5a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228947558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdc102859ece7c53edfe450e86e3c45f24fae61af9c366420100d6702618534`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:49:22 GMT
ENV NEO4J_SHA256=d7d215dcdbb9e5d6bb426003d62a1be2ffe3cb20039bb3432be8f9eab9be9e56 NEO4J_TARBALL=neo4j-enterprise-3.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:49:22 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.15-unix.tar.gz
# Fri, 17 Apr 2020 10:49:24 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.15-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:49:24 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:49:42 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:49:43 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:49:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:49:44 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:49:44 GMT
COPY file:e07128b8290e38440521f56bbf78b61bbce8be21a97b8b31668594bebdd2bf2b in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:49:45 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:49:45 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:49:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd175aae919621cd1da39eb257d49c1992019ebc58e4299c54c0a3eac4731c9`  
		Last Modified: Fri, 17 Apr 2020 11:06:45 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b131331d14745fb2930d7f90a0c90d73c88ea9ab212b922cf56438504277c5fb`  
		Last Modified: Fri, 17 Apr 2020 11:06:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7086275dca23138c316d82c133ff025c8c3a20db26a4a5f1354afbe3be3280`  
		Last Modified: Fri, 17 Apr 2020 11:07:00 GMT  
		Size: 158.0 MB (158001409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496d088741b8c58ec4ad28a826771b627675b6af758b5649e1999d3f572f19f0`  
		Last Modified: Fri, 17 Apr 2020 11:06:44 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.16`

```console
$ docker pull neo4j@sha256:526b69d75201046386e149bae5628e9d08fc5ecf63e41cdce344a3977fb36004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.16` - linux; amd64

```console
$ docker pull neo4j@sha256:8edd5105a242a143c431d1e385d9de4520a4e7dbcb2a625e507137a911731cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212627939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c016ae3c33ed71d71c5469b6dcbe3951bab0c823ca26f7ce0bdb0dc46382e2`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:47:53 GMT
ENV NEO4J_SHA256=8c42ebe3455d92deedb09417dc02bcd37f5e0f13eb3f3faa5f1a5b9d4a781c7b NEO4J_TARBALL=neo4j-community-3.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:47:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.16-unix.tar.gz
# Fri, 17 Apr 2020 10:47:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.16-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:47:56 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:48:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:48:15 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:48:15 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:48:16 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:48:16 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:48:16 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:48:17 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:48:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b7ac544e96ece52ddedd523b01398d5a0f2b3795d1aef3453aebb6d92f71ae`  
		Last Modified: Fri, 17 Apr 2020 11:04:56 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ea2f5c1217b5380a9eac8d0f5d4abc96a024968e0161e4b7e265ef92c8eed7`  
		Last Modified: Fri, 17 Apr 2020 11:04:56 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0417581e9f3ae3759e07b2eb70ce740df6c5d23df71b049b5fe19259a641a`  
		Last Modified: Fri, 17 Apr 2020 11:05:16 GMT  
		Size: 141.7 MB (141680655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e3dbd5a0a5d2c376a29ebd747abc285655b644f2850a6026fc674b5e746901`  
		Last Modified: Fri, 17 Apr 2020 11:04:56 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.16-enterprise`

```console
$ docker pull neo4j@sha256:8b1c4326ad97c5b5095cd34bdc90a69f2bff7608d57c77196a472aa79330b7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:60f8f745b57bac3b90d634651b6ab06f687616f94fad0bc75059089538e993f0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229409655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7908bc07f9f23f391204ccfa030aa6d0ad27ede892a577ce49381e75fb30bc`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:48:23 GMT
ENV NEO4J_SHA256=ba8cf11ba8eb689755fcb7aacedf74391c6b5ec9ff423e921948ace401db12b9 NEO4J_TARBALL=neo4j-enterprise-3.4.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:48:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.16-unix.tar.gz
# Fri, 17 Apr 2020 10:48:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.16-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:48:26 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:48:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:48:45 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:48:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:48:46 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:48:46 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:48:47 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:48:47 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:48:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7903c308176591dd9194a897db663a7335344617bb6e65809f0de6bc08c80ba5`  
		Last Modified: Fri, 17 Apr 2020 11:05:24 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c1154e95aa392afd2421c98a56fbe86349580f90dd1cc2a4a20893d0cb5d82`  
		Last Modified: Fri, 17 Apr 2020 11:05:24 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e336aac3d159763a9631a08b853043cf598d55e35f48dee1818eb5558aa518ba`  
		Last Modified: Fri, 17 Apr 2020 11:06:04 GMT  
		Size: 158.5 MB (158462372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4df2b22972a421657413493fdbb2fbbc0f39b3d659728dc3a5f2c216d978b7`  
		Last Modified: Fri, 17 Apr 2020 11:05:23 GMT  
		Size: 5.3 KB (5302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.17`

```console
$ docker pull neo4j@sha256:f231661818c47c3f9cbbad33ab4000d144dc4697bf7f6ad9db35ff845ee97f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.17` - linux; amd64

```console
$ docker pull neo4j@sha256:af91be2aa9869f48b59b0ef2118a536c201e3c9aef23e5da3f4611d62d4881a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215029509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d9ebb1497baaebf7b454ce11ca585e535a02a17f854ab8736f93a9af412033`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:47:03 GMT
ENV NEO4J_SHA256=fbb03e85a09e1e8a77c496ad61e8094ef94185268098634a4aaf1d1a01b841a6 NEO4J_TARBALL=neo4j-community-3.4.17-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:47:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
# Fri, 17 Apr 2020 10:47:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:47:04 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:47:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:47:19 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:47:19 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:47:19 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:47:19 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:47:19 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:47:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b73a9e13152369d2a8d23cbbd48b68a43f9f4f4b947d37972d89698082c867`  
		Last Modified: Fri, 17 Apr 2020 11:04:05 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7caf4345bc78392116bd6f04a8ca7c35474d93b48e32aff09cdf0e9a90d7cecd`  
		Last Modified: Fri, 17 Apr 2020 11:04:05 GMT  
		Size: 303.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b76a20cc81b87ff0ac245aaa6ce6ccff43d0e9bb65c4c2d92c852585186c2f2`  
		Last Modified: Fri, 17 Apr 2020 11:04:30 GMT  
		Size: 144.1 MB (144082226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871e8789435b28b1ddee002e20939bcc9476d4fdf1bdfd02edddb924d96c825b`  
		Last Modified: Fri, 17 Apr 2020 11:04:05 GMT  
		Size: 5.3 KB (5302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.17-enterprise`

```console
$ docker pull neo4j@sha256:9a481383a71094a0a1a584d446fb040cfee5802d42cf983a7a145bece8bef837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.17-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:38f3e9fa2107f57e48c82f34849f4bd963dfd78e6d46126ad586610c37849271
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231812854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cde34240da18107c9cf49f4586f9e9333b191f9abadb3cf1e90455e61f0938`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:47:23 GMT
ENV NEO4J_SHA256=7d8d689ddc605c66296fadedb0d6810b8159513cb596b68b730f2604ce8bb9df NEO4J_TARBALL=neo4j-enterprise-3.4.17-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:47:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
# Fri, 17 Apr 2020 10:47:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:47:28 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:47:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:47:45 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:47:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:47:45 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:47:46 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:47:46 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:47:46 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:47:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f89d715feb6b9ae2b20a70a5e4cd3de313ec353472e49ae7f411865d044b02`  
		Last Modified: Fri, 17 Apr 2020 11:04:35 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121bc4ee5f67854d3c5c954cd4e8ec8452ad7ca03306665c75c0552ce5518ba5`  
		Last Modified: Fri, 17 Apr 2020 11:04:35 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18427b51f2e3d32e7585d53296553ce34b3ea8a2c6d8ad26a1cc79ceaa9aeec3`  
		Last Modified: Fri, 17 Apr 2020 11:04:52 GMT  
		Size: 160.9 MB (160865571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb0c03b5c5bc6e0ee1286c6f9fa56a4d6901bee965814c23a37bab420a4c26c`  
		Last Modified: Fri, 17 Apr 2020 11:04:35 GMT  
		Size: 5.3 KB (5302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4-enterprise`

```console
$ docker pull neo4j@sha256:9a481383a71094a0a1a584d446fb040cfee5802d42cf983a7a145bece8bef837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:38f3e9fa2107f57e48c82f34849f4bd963dfd78e6d46126ad586610c37849271
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231812854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cde34240da18107c9cf49f4586f9e9333b191f9abadb3cf1e90455e61f0938`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:47:23 GMT
ENV NEO4J_SHA256=7d8d689ddc605c66296fadedb0d6810b8159513cb596b68b730f2604ce8bb9df NEO4J_TARBALL=neo4j-enterprise-3.4.17-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:47:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
# Fri, 17 Apr 2020 10:47:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:47:28 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:47:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:47:45 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:47:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:47:45 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:47:46 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:47:46 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:47:46 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:47:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f89d715feb6b9ae2b20a70a5e4cd3de313ec353472e49ae7f411865d044b02`  
		Last Modified: Fri, 17 Apr 2020 11:04:35 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121bc4ee5f67854d3c5c954cd4e8ec8452ad7ca03306665c75c0552ce5518ba5`  
		Last Modified: Fri, 17 Apr 2020 11:04:35 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18427b51f2e3d32e7585d53296553ce34b3ea8a2c6d8ad26a1cc79ceaa9aeec3`  
		Last Modified: Fri, 17 Apr 2020 11:04:52 GMT  
		Size: 160.9 MB (160865571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb0c03b5c5bc6e0ee1286c6f9fa56a4d6901bee965814c23a37bab420a4c26c`  
		Last Modified: Fri, 17 Apr 2020 11:04:35 GMT  
		Size: 5.3 KB (5302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5`

```console
$ docker pull neo4j@sha256:6f937c15f6260b0227ffab66e28192e41e1635211f5e07dd0af104d47867f8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5` - linux; amd64

```console
$ docker pull neo4j@sha256:31b44871c6aba8d10a90c6e2ea1f070c7cf8b2fba4c5be207a70d0b558d1bf4f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206787465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8716e9799f242e7625e13211a449d764ec6f4c33c8b6c84ef97ed0f00976ba`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:37:32 GMT
ENV NEO4J_SHA256=1c8b6ac0ffd346f0707fe1af713ef74f1c6ce1ea6feb5e9a0bd170e7a8a34a10 NEO4J_TARBALL=neo4j-community-3.5.17-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:37:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
# Fri, 17 Apr 2020 10:37:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:37:35 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:37:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:37:58 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:37:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:37:58 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:37:59 GMT
COPY file:cd969a3e3d21f58e9a9a346d321ec15de0b681e0976dc4b74a6a00cb6cd0f32c in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:37:59 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:37:59 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:38:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a990155a45f3aa55c8bba679a505f417860404c870cf4f3be393d691cb2a4b56`  
		Last Modified: Fri, 17 Apr 2020 10:55:16 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75eed058e0d5624417d2365babb5bf712aa08687eab86c40cc2086a6d6601e3`  
		Last Modified: Fri, 17 Apr 2020 10:55:16 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f198547a71b0e5efbdb03be0fb9ef8caa054ffbc9083909c880dd55e878cfa`  
		Last Modified: Fri, 17 Apr 2020 10:55:34 GMT  
		Size: 135.8 MB (135839456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b16ca905db0a46918ce24ac8a35553b63e1c5e1cdf4c29815b72d35fc6d78f3`  
		Last Modified: Fri, 17 Apr 2020 10:55:16 GMT  
		Size: 5.9 KB (5881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.11`

```console
$ docker pull neo4j@sha256:ea3222806100d592bc83356e4dce33ccc6c16224d299c9b8a2c769eda648cf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.11` - linux; amd64

```console
$ docker pull neo4j@sha256:6b5c8e893f7d675882514d2486b2dce81aa8f8f54371502c1a1171b9a8ea9f18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228140613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85590ceb82a0d3ffedbef34c5fb6002496d7fb199a783f47fbcbfeeba68f102`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:43:24 GMT
ENV NEO4J_SHA256=4dd4f2b6c32e216b42ab8d2235f10c4d992d567d36927df93d2d9fb1763e6376 NEO4J_TARBALL=neo4j-community-3.5.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:43:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.11-unix.tar.gz
# Fri, 17 Apr 2020 10:43:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.11-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:43:26 GMT
COPY multi:7cf12d6a82ce8caa397305af40147113f0c2e3f75bed74dbe4e434adf3288487 in /tmp/ 
# Fri, 17 Apr 2020 10:43:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:43:45 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:43:45 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:43:46 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:43:46 GMT
COPY file:8d85ed1b091a881aa7d34786c77b3933cd5f54de55a2d3f2248786eef97d873d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:43:46 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:43:47 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:43:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfac61761224ff539490fd7481446a6052c229316515def83b50c962c7afe83`  
		Last Modified: Fri, 17 Apr 2020 10:59:52 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3f2ae0bc4c95b5acb2ebf26db0322ef34f08302c4a7d41748374997f57eb2`  
		Last Modified: Fri, 17 Apr 2020 10:59:52 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b2113d7285900e042ac09757d0522d841763f827d75f6daac867ff8bbc0326`  
		Last Modified: Fri, 17 Apr 2020 11:00:09 GMT  
		Size: 157.2 MB (157193384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46478f1fdfe241120461c37721535c705418a25bdd423bd1c1fb529d103b42cb`  
		Last Modified: Fri, 17 Apr 2020 10:59:52 GMT  
		Size: 5.2 KB (5250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.11-enterprise`

```console
$ docker pull neo4j@sha256:a8da1a25abb85d818fd236cfa29ebf3300eea6fd56a6ca1bfb50b39378b2d0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.11-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:732671effbbe8fa9c53ed294f652fd53b4b449f6b68eaee74d504106326f5b4a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263209167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f0af39db52ef054b06837232c7918645c6e8c5264e76bc9657beb2719507ab`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:43:53 GMT
ENV NEO4J_SHA256=e706a6a008bebc5fa06d97f671dc6099d1d1871020373c053a28f695964f88b2 NEO4J_TARBALL=neo4j-enterprise-3.5.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:43:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.11-unix.tar.gz
# Fri, 17 Apr 2020 10:43:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.11-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:43:56 GMT
COPY multi:7cf12d6a82ce8caa397305af40147113f0c2e3f75bed74dbe4e434adf3288487 in /tmp/ 
# Fri, 17 Apr 2020 10:44:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:44:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:44:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:44:17 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:44:17 GMT
COPY file:8d85ed1b091a881aa7d34786c77b3933cd5f54de55a2d3f2248786eef97d873d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:44:17 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:44:18 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:44:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d683652811e25da89e41704d209d049c68b43e1fdcf2b6ebc0b734c16d5d4940`  
		Last Modified: Fri, 17 Apr 2020 11:00:16 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effac5954f0b8e16432f36c7dc28332304f28e75be9a3982bfcbba121b952875`  
		Last Modified: Fri, 17 Apr 2020 11:00:16 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe6e8daabc92a534a78b4971b390f485b6e0ac18de7fce138ac30c04963957`  
		Last Modified: Fri, 17 Apr 2020 11:00:47 GMT  
		Size: 192.3 MB (192261921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292def6ce31bbfd5e1d180a1287e4dbccb6ef3d353affda690a9e60ee290c47e`  
		Last Modified: Fri, 17 Apr 2020 11:00:16 GMT  
		Size: 5.3 KB (5251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.12`

```console
$ docker pull neo4j@sha256:6b7ed33fb4e252b95154fa34eb22a0b95bbe539ddc85d0a8e34a2ea9d3b71cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.12` - linux; amd64

```console
$ docker pull neo4j@sha256:855dd593c62c4043edaf55a602619f63afe8bb15f5d6f947183f1481aa92c8fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228336024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d013e9994047798f5273c868f88408fc655e560c4c37d4bf84a2669dccf803`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:42:33 GMT
ENV NEO4J_SHA256=3b82b72a211d1b628b64f18f4af9f10b12ed6e2fd0ad94910e11b7fef5d0d86c NEO4J_TARBALL=neo4j-community-3.5.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:42:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.12-unix.tar.gz
# Fri, 17 Apr 2020 10:42:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.12-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:42:35 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:42:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:42:50 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:42:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:42:51 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:42:51 GMT
COPY file:8d85ed1b091a881aa7d34786c77b3933cd5f54de55a2d3f2248786eef97d873d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:42:51 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:42:51 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:42:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb5ef32bbfd5fac1ecf01a749f6fb903b63a672209826b5ec7a0a543802bb41`  
		Last Modified: Fri, 17 Apr 2020 10:59:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4545d1e6a57f8cfe309b6e16b13c5a410e68fd725ef1e88cd0ab0d25018b1580`  
		Last Modified: Fri, 17 Apr 2020 10:59:14 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3576674983f4dc41dd56c7e8dbf864cdb04b511288cf35eb8f2561396e49b271`  
		Last Modified: Fri, 17 Apr 2020 10:59:29 GMT  
		Size: 157.4 MB (157388794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7bf2f63707a640829f6416d495eccc0d7605be11e8879a8f3429e6c0265d16`  
		Last Modified: Fri, 17 Apr 2020 10:59:14 GMT  
		Size: 5.2 KB (5250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.12-enterprise`

```console
$ docker pull neo4j@sha256:237812df9bb5e7d8c7989ae2f5da48f9877243989c2b4767f23d1bb1b2aca9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.12-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:f9df83f4b2700a0a37d9fda04b9c5963e27c9683ac3dda93f161e05a0fea6069
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263452862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874c76066c85b8807147e22ded75cb76cd5f087235daa94f35c06769c213bd5a`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:42:58 GMT
ENV NEO4J_SHA256=bf23ff236aa5e4b15a840441d7e75d14ff3eb04de8e67edd291c23762be790cd NEO4J_TARBALL=neo4j-enterprise-3.5.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:42:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.12-unix.tar.gz
# Fri, 17 Apr 2020 10:42:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.12-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:42:59 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:43:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:43:15 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:43:15 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:43:16 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:43:16 GMT
COPY file:8d85ed1b091a881aa7d34786c77b3933cd5f54de55a2d3f2248786eef97d873d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:43:16 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:43:16 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:43:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cff61a217ac57806928467d56832ba3da3b5716688ac0ccf6281ee7238869fe`  
		Last Modified: Fri, 17 Apr 2020 10:59:32 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c60b47a519c79c7df40f15acae9c39e10bb3995c7887322c5b867db5ba86d7`  
		Last Modified: Fri, 17 Apr 2020 10:59:32 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0517b11cf1aacd231d96c0ed9ee2bcef5ea6d90dcc761b248517a5789ce2eea`  
		Last Modified: Fri, 17 Apr 2020 10:59:49 GMT  
		Size: 192.5 MB (192505632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4385b4c2bc17f2280aba3044be26ea625c69950630c420ddf3c12e49e2f84dfd`  
		Last Modified: Fri, 17 Apr 2020 10:59:32 GMT  
		Size: 5.2 KB (5250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.13`

```console
$ docker pull neo4j@sha256:60ce7241e4c24fad83d906ca6f50072a7c1de6e630bbda865013c29ed69a88a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.13` - linux; amd64

```console
$ docker pull neo4j@sha256:45cd86a16f06f33ecf6c0a1ba93fac41f01bc4a1e77f0e1033cd121584992393
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230552510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caad858faac734c6d5a41b7edda0da95c5e7ea3afd1f662fb1b6a35d8d36162`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:41:43 GMT
ENV NEO4J_SHA256=2fdb29816bc72894b10f082b5d542fdaa0cf5d9cfdb899d9aac1e34bc2006250 NEO4J_TARBALL=neo4j-community-3.5.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:41:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.13-unix.tar.gz
# Fri, 17 Apr 2020 10:41:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.13-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:41:44 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:42:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:42:02 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:42:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:42:03 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:42:03 GMT
COPY file:af001fe5ddb05cac858c69f075bc3cd9077701dfa2891fe6c5a518755a596997 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:42:03 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:42:03 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:42:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a31c71bf790f75ebf52030d1f5670b15c0ba049ba22d2c2a9b049bfe656b4ac`  
		Last Modified: Fri, 17 Apr 2020 10:58:37 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f77147f02de6b52c0963f43da3402be94783b54c67cb519d6587aadb8652103`  
		Last Modified: Fri, 17 Apr 2020 10:58:37 GMT  
		Size: 303.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aae10d5e9ff2b9b592ca4f4152d38fad5996aadb75779cd6ec5d832f972e1b8`  
		Last Modified: Fri, 17 Apr 2020 10:58:52 GMT  
		Size: 159.6 MB (159605274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9856bed7ac5df7d069323a9a946cfe6b4977519381483c049df99adf695f346f`  
		Last Modified: Fri, 17 Apr 2020 10:58:37 GMT  
		Size: 5.3 KB (5252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.13-enterprise`

```console
$ docker pull neo4j@sha256:cf08c2d3464f68d66ea179cc9dbd70e23effa45e2b5c2b6dae48ddf3143506e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.13-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fb1df52f4d9142481f707c38fa65bb6c32b39b155d10bba95b994ad5ea695b0a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265679824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebae2146159f708638a97d334a7094ab5c873d9147a3e51c302c66c9e3ceb7b`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:42:08 GMT
ENV NEO4J_SHA256=e1f74ed3923dc65498f4bf8b17a41d4e05e505e093c23e65ab3e6c47d1ca61af NEO4J_TARBALL=neo4j-enterprise-3.5.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:42:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.13-unix.tar.gz
# Fri, 17 Apr 2020 10:42:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.13-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:42:09 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:42:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:42:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:42:26 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:42:26 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:42:26 GMT
COPY file:af001fe5ddb05cac858c69f075bc3cd9077701dfa2891fe6c5a518755a596997 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:42:26 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:42:26 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:42:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6429c73b194e7f50f366f2ce5198c2b7795938930ecad18c3c8209e5d20ecbe2`  
		Last Modified: Fri, 17 Apr 2020 10:58:56 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78589109f593e5fcb10eb0e89de1d4e4e526f247eff4d8e683a2f60fd047669a`  
		Last Modified: Fri, 17 Apr 2020 10:58:56 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5208ef4c0605ed389b798b883e61d0d031fdbaacb025be9149c3d7d517d9f5`  
		Last Modified: Fri, 17 Apr 2020 10:59:10 GMT  
		Size: 194.7 MB (194732594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbafc4aad2474a0791e42f843470d2e56fda03c48a84e92ad95c5f456e6ecf15`  
		Last Modified: Fri, 17 Apr 2020 10:58:56 GMT  
		Size: 5.3 KB (5252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.14`

```console
$ docker pull neo4j@sha256:5e72af7d6f3eba9bf048878e5e69990e6905dcee1a0aafd61913b73823d70ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.14` - linux; amd64

```console
$ docker pull neo4j@sha256:27937b4581d92fa7baf73d09fe87e64b1be6b247674d4268fc5f7190bca6cd40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229467636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ab0c61b7f9096b86a52d73513794a4764377d2d0401f62ea68b272e24c722f`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:40:53 GMT
ENV NEO4J_SHA256=fb435b11494cde475f748f057a192bcbd8580c7445b380afe9ff52311f334bfe NEO4J_TARBALL=neo4j-community-3.5.14-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:40:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.14-unix.tar.gz
# Fri, 17 Apr 2020 10:40:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.14-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:40:54 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:41:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.14-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:41:10 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:41:10 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:41:10 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:41:10 GMT
COPY file:7ffb493993f443c8153ccfe7de8510ab04c58686ca8ed69aed987a3e80542d26 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:41:11 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:41:11 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:41:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e565f6e53ef67e68ed25b0ca5748bc0a234d45f3d5461e1504af8050aed2b6e1`  
		Last Modified: Fri, 17 Apr 2020 10:57:37 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1adb6f5fcbdeb4e683387c4771e41c61a7c7d54067ba309fd38ba2d041ef17a`  
		Last Modified: Fri, 17 Apr 2020 10:57:37 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e126f6b00014a39c83878093ac0ccf3e10a56e1b5dae526b849f4f2e259bcb`  
		Last Modified: Fri, 17 Apr 2020 10:58:01 GMT  
		Size: 158.5 MB (158520245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fb29a97cf2ff10160c3a7d95ca9f21495f6a37385c561d4b9d0b1a0fd884e0`  
		Last Modified: Fri, 17 Apr 2020 10:57:37 GMT  
		Size: 5.4 KB (5412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.14-enterprise`

```console
$ docker pull neo4j@sha256:0f47826a0251b27a8814216674cb162f1e3d67b723f615cc2d7d38d1a9c6bf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.14-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:de22e4e7fce8d4795b6d74c95bc3770bc4ec1ae299cad75b01ded4b0d0b6c1b2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264586286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8cfe36871191f5b3df8fbcbc945e7ae3734d5371d1f4c399cc16d2f453577d`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:41:18 GMT
ENV NEO4J_SHA256=8d02047f3196c23849f7b6dda605b98098dbdc694747f1708e119715af3d3e06 NEO4J_TARBALL=neo4j-enterprise-3.5.14-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:41:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.14-unix.tar.gz
# Fri, 17 Apr 2020 10:41:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.14-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:41:19 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 17 Apr 2020 10:41:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.14-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:41:37 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:41:37 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:41:38 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:41:38 GMT
COPY file:7ffb493993f443c8153ccfe7de8510ab04c58686ca8ed69aed987a3e80542d26 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:41:38 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:41:38 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:41:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042ce59f68bc809583f5c49c5511068649f6a891feaae949057031d04b3ffc2f`  
		Last Modified: Fri, 17 Apr 2020 10:58:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d6006af558de42d1e0f4717df9cebfd40826177540f471788df9f7c247f701`  
		Last Modified: Fri, 17 Apr 2020 10:58:06 GMT  
		Size: 301.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31249652f291e8172940eac9fed7f33521addcb39e2afe48cf0ebd25d1f9f6b8`  
		Last Modified: Fri, 17 Apr 2020 10:58:33 GMT  
		Size: 193.6 MB (193638893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8190148ae60782d4b0ebcc857c26bf1b8c9bfbfcc7f28207787d86ef22462e7e`  
		Last Modified: Fri, 17 Apr 2020 10:58:06 GMT  
		Size: 5.4 KB (5411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.15`

```console
$ docker pull neo4j@sha256:3fbc26474699b9d2d9499bb1bf2a35a194213492f7cd1ac43b39dd9c4ad6d516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.15` - linux; amd64

```console
$ docker pull neo4j@sha256:91d87ca6643de5caeb55193f57a3051e5e0471109c8491ce1f22f6d3ac4628db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206733465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64f849cc30b8d36d1c7001fd8fe546e43a60902c939dcbe12a954f3e5f177fd`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:39:45 GMT
ENV NEO4J_SHA256=32ed30e81aed0fc32d7ca8245b4a25e7aa1c08b89770ea33da1f4b427f1f7664 NEO4J_TARBALL=neo4j-community-3.5.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:39:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.15-unix.tar.gz
# Fri, 17 Apr 2020 10:39:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.15-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:39:47 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:40:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.15-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:40:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:40:09 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:40:10 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:40:10 GMT
COPY file:2302715b081c832649219f56c02e31f4562056b8ba8cd7c7dd5e1cf549d9e537 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:40:10 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:40:11 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:40:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf3e48913d4927c14dd90e910a993ccdb7f9b9c99aaeeafebbab5d7e80a3051`  
		Last Modified: Fri, 17 Apr 2020 10:56:51 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b751ab6dfab2dab03ef2d8fda424c14ed22aaa87055cd4c237f090a304f5c713`  
		Last Modified: Fri, 17 Apr 2020 10:56:51 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e28c6bc0386ee1b1652fed7a46b7975fc379c9fcfad53de0f7305617a2e5ce`  
		Last Modified: Fri, 17 Apr 2020 10:57:09 GMT  
		Size: 135.8 MB (135785454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7f471879d8f223075dd8d12cea702e674380e4b0e028a71da98112fc9d6a23`  
		Last Modified: Fri, 17 Apr 2020 10:56:51 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.15-enterprise`

```console
$ docker pull neo4j@sha256:daf9785370a339326916eeebb66359fb94fc6ea590491418ed174366302aa3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0f10a35374f98f9bf58d7eb35024be0bf7c46df2767859b8bb0c153d8430793a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241861713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029c50525e33ba6433e4764fa12dd3d128247573af405372658b6a901864f541`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:40:19 GMT
ENV NEO4J_SHA256=0d179b9e7f15c9d63a4b488976117012320b7ba6c8d9ccdca16342d392ea820a NEO4J_TARBALL=neo4j-enterprise-3.5.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:40:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.15-unix.tar.gz
# Fri, 17 Apr 2020 10:40:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.15-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:40:21 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:40:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.15-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:40:43 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:40:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:40:44 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:40:44 GMT
COPY file:2302715b081c832649219f56c02e31f4562056b8ba8cd7c7dd5e1cf549d9e537 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:40:44 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:40:45 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:40:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c59fbcf9d2902b3e75eeda446bb80b538e78f58c7d58bbaf51c7232c3d3f12`  
		Last Modified: Fri, 17 Apr 2020 10:57:14 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd10aa75c8c8c960d4f48fba2ee96f7b947773eaae28fe4322aed22a907426b`  
		Last Modified: Fri, 17 Apr 2020 10:57:14 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274156f003f19276e54f885ff27868b1245be68367b8fd1e5b8091244cdb4f1`  
		Last Modified: Fri, 17 Apr 2020 10:57:33 GMT  
		Size: 170.9 MB (170913700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4973172c58092c568c69cfac09c389f00474e39c8ca8fee0abcd53fe1c50ca43`  
		Last Modified: Fri, 17 Apr 2020 10:57:14 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.16`

```console
$ docker pull neo4j@sha256:c058e2066a2346ea0a04bb3ea5587669bb3f99b01f172991c77f18ffe76ec600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.16` - linux; amd64

```console
$ docker pull neo4j@sha256:9767e9d38bf08c53af3b22caa5044320cb7f36950f3b059f7e9648ecb6e930fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206739382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f5fb69078d9fddd44e5c5e1ec2797acb331d1faf3bbb96dfbe143a14c300c1`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:38:41 GMT
ENV NEO4J_SHA256=3eded9065de1ddd39d519b05845da2f572b5ddb4e6440b93555927f329eaf222 NEO4J_TARBALL=neo4j-community-3.5.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:38:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.16-unix.tar.gz
# Fri, 17 Apr 2020 10:38:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.16-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:38:43 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:39:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.16-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:39:03 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:39:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:39:04 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:39:04 GMT
COPY file:2302715b081c832649219f56c02e31f4562056b8ba8cd7c7dd5e1cf549d9e537 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:39:04 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:39:05 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:39:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23217af1dda5a586d2c01c0481924928d9125e93cf1d39200795ad0c7e961da`  
		Last Modified: Fri, 17 Apr 2020 10:56:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb514e751ca6202ea265a9e59f1f9a9fda5a3edae4b6e2098510de03cffe4976`  
		Last Modified: Fri, 17 Apr 2020 10:56:04 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cc4d27a925b1fa80d0ee664a8a03b11093a08dbcd7b3b44733b6460c9200b4`  
		Last Modified: Fri, 17 Apr 2020 10:56:24 GMT  
		Size: 135.8 MB (135791368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a759a23e04c5ccca4a8ed729710cb10c13ea8d8562449477fc2558dd292830`  
		Last Modified: Fri, 17 Apr 2020 10:56:04 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.16-enterprise`

```console
$ docker pull neo4j@sha256:72d8cbca9759f22f1cf5e825dd32fe1c8f4df25094f4651ca70022b89aa19156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ad6f6caefca9101cba55941f514da41d0f312023268c9fd319edcbcef1e084af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241870480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff699a3074c3bd795a189ef7be48933aa9286638e82a4ddbd321e756724f5e1b`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:39:11 GMT
ENV NEO4J_SHA256=38dfbaa88b2b17eeb8ec7cf4362327b08f04dd2733374541ba6f233fba6560b2 NEO4J_TARBALL=neo4j-enterprise-3.5.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:39:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.16-unix.tar.gz
# Fri, 17 Apr 2020 10:39:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.16-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:39:13 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:39:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.16-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:39:35 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:39:35 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:39:36 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:39:36 GMT
COPY file:2302715b081c832649219f56c02e31f4562056b8ba8cd7c7dd5e1cf549d9e537 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:39:36 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:39:37 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:39:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd30e85e84462dea9e99ca4f487ce0b75008590257c64eb9b25f39ce706cb6c2`  
		Last Modified: Fri, 17 Apr 2020 10:56:28 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd199d9fade5fe11a68dcd7cdc9ef9a64bbd0f33bb996b5b7da412a101558ce7`  
		Last Modified: Fri, 17 Apr 2020 10:56:28 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57d563ffc089c514748a2c6f0d49769125e829fac831875a0d618448a143f5`  
		Last Modified: Fri, 17 Apr 2020 10:56:46 GMT  
		Size: 170.9 MB (170922465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a10a6508650714f81122221a2019ee4125814eaffb44d16b25ffa41f6b6c26`  
		Last Modified: Fri, 17 Apr 2020 10:56:28 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.17`

```console
$ docker pull neo4j@sha256:6f937c15f6260b0227ffab66e28192e41e1635211f5e07dd0af104d47867f8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.17` - linux; amd64

```console
$ docker pull neo4j@sha256:31b44871c6aba8d10a90c6e2ea1f070c7cf8b2fba4c5be207a70d0b558d1bf4f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206787465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8716e9799f242e7625e13211a449d764ec6f4c33c8b6c84ef97ed0f00976ba`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:37:32 GMT
ENV NEO4J_SHA256=1c8b6ac0ffd346f0707fe1af713ef74f1c6ce1ea6feb5e9a0bd170e7a8a34a10 NEO4J_TARBALL=neo4j-community-3.5.17-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:37:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
# Fri, 17 Apr 2020 10:37:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:37:35 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:37:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:37:58 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:37:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:37:58 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:37:59 GMT
COPY file:cd969a3e3d21f58e9a9a346d321ec15de0b681e0976dc4b74a6a00cb6cd0f32c in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:37:59 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:37:59 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:38:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a990155a45f3aa55c8bba679a505f417860404c870cf4f3be393d691cb2a4b56`  
		Last Modified: Fri, 17 Apr 2020 10:55:16 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75eed058e0d5624417d2365babb5bf712aa08687eab86c40cc2086a6d6601e3`  
		Last Modified: Fri, 17 Apr 2020 10:55:16 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f198547a71b0e5efbdb03be0fb9ef8caa054ffbc9083909c880dd55e878cfa`  
		Last Modified: Fri, 17 Apr 2020 10:55:34 GMT  
		Size: 135.8 MB (135839456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b16ca905db0a46918ce24ac8a35553b63e1c5e1cdf4c29815b72d35fc6d78f3`  
		Last Modified: Fri, 17 Apr 2020 10:55:16 GMT  
		Size: 5.9 KB (5881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.17-enterprise`

```console
$ docker pull neo4j@sha256:2cc81823dedee03da4d4a33af2eecff9c86ff8a762423745d85bd8bbc8763b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.17-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:21ee092f9025d6648b9a5966b588737bd169962c06041730cb9ffa279362f28a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241919044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967769430a35570a48340a2319abe7b3f6c659e85b12829f3bd4e4324c3e4ad3`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:38:06 GMT
ENV NEO4J_SHA256=1f8c60e01e8bcdb5c6921341bd4a783c08a748cabb3348d4e4d2f104544232ca NEO4J_TARBALL=neo4j-enterprise-3.5.17-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:38:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
# Fri, 17 Apr 2020 10:38:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:38:09 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:38:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:38:31 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:38:32 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:38:32 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:38:32 GMT
COPY file:cd969a3e3d21f58e9a9a346d321ec15de0b681e0976dc4b74a6a00cb6cd0f32c in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:38:33 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:38:33 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:38:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819d6d2030d11093838d230ecfd42825ddf2ecb6e141d242c88b80c8b8b0598e`  
		Last Modified: Fri, 17 Apr 2020 10:55:41 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e18d3303ad288c4a4315c064fe3eee34d8d2823313e716e0f863f6ca9461da`  
		Last Modified: Fri, 17 Apr 2020 10:55:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0d4827533f72fafef05f4c9232cdfafd235ad5100e5584f18a3d24e088875c`  
		Last Modified: Fri, 17 Apr 2020 10:55:59 GMT  
		Size: 171.0 MB (170971030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce86cc8a14c300a3b29c6bb84dd110d7907af09c87d4e3f698d69451996555c`  
		Last Modified: Fri, 17 Apr 2020 10:55:41 GMT  
		Size: 5.9 KB (5881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.6`

```console
$ docker pull neo4j@sha256:f03e25fa66dcefdf1334d4b4985afaae9349ab8f5f8ebeca39e353e8b1930e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.6` - linux; amd64

```console
$ docker pull neo4j@sha256:7b5751b061054899affaed1086d57a666a30fa1c77cd0e4c25bcc714da562f7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240874260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cf2fc4c848c6d107658169bd4d4109e8e112f1f36bf12f255bfe46ac929756`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:46:16 GMT
ENV NEO4J_SHA256=f536224565ce27b95947c91a37d52b9ba9e80247d8d3262075b24b8d47f8532a NEO4J_TARBALL=neo4j-community-3.5.6-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:46:16 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.6-unix.tar.gz
# Fri, 17 Apr 2020 10:46:17 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.6-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:46:17 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:46:31 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.6-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 17 Apr 2020 10:46:31 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:46:31 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:46:31 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:46:32 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:46:32 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:46:32 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:46:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4289f6980ec5d35172f21f7323bdc2349379bca9ab659b9e38abf869b8ea5b`  
		Last Modified: Fri, 17 Apr 2020 11:03:18 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e915ca0339350c3e7b7e0b96caae241abef4bdc1adb68c55942299f893446922`  
		Last Modified: Fri, 17 Apr 2020 11:03:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9295f1ecda71cb15ad4a6d53a5bda3d71c79b6462691887875e9b2cd41ca5acf`  
		Last Modified: Fri, 17 Apr 2020 11:03:35 GMT  
		Size: 169.9 MB (169928067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e3f09e5097f5472689a6accf2cc847362f4077b3f00eb29ab6d26b5bf1052c`  
		Last Modified: Fri, 17 Apr 2020 11:03:17 GMT  
		Size: 4.4 KB (4386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.6-enterprise`

```console
$ docker pull neo4j@sha256:c83c62e10e5d014ca1c02c9385636bd8ad3cb225774c5dc90b532b6d6d2c04d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.6-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:59d6634f07914f35235427a7674bfb8f2de8ef71482843b804b9b19ab39a43c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (275971758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9b9d05ec1e049b801f13d495be9e146a03a9cc1857becc6ca365dcc5323d91`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:46:37 GMT
ENV NEO4J_SHA256=0d738dd5bd04aaf15c672e27833480339de5bbe85a56cc932bd15aa27fb99509 NEO4J_TARBALL=neo4j-enterprise-3.5.6-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:46:37 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.6-unix.tar.gz
# Fri, 17 Apr 2020 10:46:38 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.6-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:46:38 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:46:55 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.6-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 17 Apr 2020 10:46:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:46:55 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:46:56 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:46:56 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:46:56 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:46:56 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:46:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f784bf5514a262e6b5d81f22c0c8d8ba890b55e8b9bb42fff790dc618ec9103`  
		Last Modified: Fri, 17 Apr 2020 11:03:40 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab46c916fbe3e9878a5ca33263d9cc5b2748dd382d269f7d7ffaa743d205d3fd`  
		Last Modified: Fri, 17 Apr 2020 11:03:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669b4e454a409b988780adbf196145071ee21dd4afe40b8dd81ebf177d389a2d`  
		Last Modified: Fri, 17 Apr 2020 11:04:01 GMT  
		Size: 205.0 MB (205025564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aebfafb65c6fee0f1fe30a2ac86f07041aef8f41af666c076f15007bedd59d9`  
		Last Modified: Fri, 17 Apr 2020 11:03:40 GMT  
		Size: 4.4 KB (4386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.7`

```console
$ docker pull neo4j@sha256:9b297d5a4551ce0f23379eafa4d05da846d369df47d110e51b68bd130f96a4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.7` - linux; amd64

```console
$ docker pull neo4j@sha256:ba42e6d0962d079aa25bf48aea276c594bf9fab158c3bac3e6b98f3067fe2534
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240938910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d24f08671f911c0d096b53517f3093817685037a06c332fe9fd69228160aa52`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:45:22 GMT
ENV NEO4J_SHA256=31c8f398df9342928502a7321f045eb8f2b96ec4ded26f9f057dc6f6fa10c60c NEO4J_TARBALL=neo4j-community-3.5.7-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:45:22 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.7-unix.tar.gz
# Fri, 17 Apr 2020 10:45:24 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.7-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:45:24 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:45:43 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.7-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 17 Apr 2020 10:45:43 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:45:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:45:43 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:45:44 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:45:44 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:45:44 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:45:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d6457084d197dd92b7d8d885283515f3a929599b4ec05a96ee2868050d680f`  
		Last Modified: Fri, 17 Apr 2020 11:02:24 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87db7724389bc49695b6f2036a9148e2a42d9fd3de45e1f4f2ab7e227ca551ef`  
		Last Modified: Fri, 17 Apr 2020 11:02:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ac50d2a340664819b4e2d541e848b971e533eed972246f1c66a39eb072e3cf`  
		Last Modified: Fri, 17 Apr 2020 11:02:42 GMT  
		Size: 170.0 MB (169992718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7551e4af9dccd59871224b8c2280401e490dcd5f19298622b9e8fb043a8e3150`  
		Last Modified: Fri, 17 Apr 2020 11:02:24 GMT  
		Size: 4.4 KB (4385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.7-enterprise`

```console
$ docker pull neo4j@sha256:e0743f7a5c933b01dc9a2e776ad8b82d28069343b2a0bc97e0e782a8bf975187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.7-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:535cfeb791f07fdf20e4a3586b7be1a1921a8892bd0cd3c73b6c1486ec48232c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276066819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2ec829bf0a81999bbc75e4fb94310676625722d638e01bf52cd794727656e4`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:45:51 GMT
ENV NEO4J_SHA256=f4585c82e43c52d06db3c4194a62766c20adea3566fcc9e9992e3f19d3311e14 NEO4J_TARBALL=neo4j-enterprise-3.5.7-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:45:51 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.7-unix.tar.gz
# Fri, 17 Apr 2020 10:45:52 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.7-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:45:53 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:46:10 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.7-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 17 Apr 2020 10:46:10 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:46:10 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:46:10 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:46:10 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:46:11 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:46:11 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:46:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286c0f97a34944c6f418281b721b5fdf7102151f42f7ca44754bca7b6488a291`  
		Last Modified: Fri, 17 Apr 2020 11:02:46 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5623d117199270f4366aac566a394e9f9e808513c623bbc329d2ee10f203d18f`  
		Last Modified: Fri, 17 Apr 2020 11:02:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46ea32b074ba9432aa259a42498d8b63dbb0d4a922ca65adeddadc42d6e49da`  
		Last Modified: Fri, 17 Apr 2020 11:03:11 GMT  
		Size: 205.1 MB (205120629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41167e060021b16fb22d5a225b9817bcf6642d73ba2f12941dfb1337d4cff949`  
		Last Modified: Fri, 17 Apr 2020 11:02:46 GMT  
		Size: 4.4 KB (4387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.8`

```console
$ docker pull neo4j@sha256:6d4f83334390ecb9c5bb55d9e71360413a5545c62c2d74f7a8a239807408f3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.8` - linux; amd64

```console
$ docker pull neo4j@sha256:dc0746bc7c8dd362364afe686bc587d63a7bdf0614d7b3590b4dc45abb8beed8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227562359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ce831fe6bb4d28323a8ad3d84f8b1a3f7cda4b132d4e98221f909bb3f57e96`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:44:23 GMT
ENV NEO4J_SHA256=ef714d0e7067d437649e52b6727d258c46a144db2ce567dc4d13b62ee916494e NEO4J_TARBALL=neo4j-community-3.5.8-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:44:23 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.8-unix.tar.gz
# Fri, 17 Apr 2020 10:44:25 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.8-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:44:25 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:44:43 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.8-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:44:44 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:44:44 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:44:44 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:44:45 GMT
COPY file:e07128b8290e38440521f56bbf78b61bbce8be21a97b8b31668594bebdd2bf2b in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:44:45 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:44:45 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256c0d68f8286835aef74258758ce4d2476eaa3146443afdf66bf8509501a32a`  
		Last Modified: Fri, 17 Apr 2020 11:00:54 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb935d09f772fa0a4678c8c849bb6d9bff206dc732fca6e67d7dace2a91cd9e9`  
		Last Modified: Fri, 17 Apr 2020 11:00:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb4657132abeb608d0240135b5a20cfaa3bd1885a38450821da9e4765cbac62`  
		Last Modified: Fri, 17 Apr 2020 11:01:34 GMT  
		Size: 156.6 MB (156616203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4752c4986fdb4a64e4b5d4073d90855a5134f496360866616f214ffddfaf8`  
		Last Modified: Fri, 17 Apr 2020 11:00:54 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.8-enterprise`

```console
$ docker pull neo4j@sha256:364218596e32a79028d83e95e39f831060ca4e8efb8dd04279d7b325b4779697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.8-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2bf56f983c29639c261e78027bf45a7662603a49af0e6bce88279779b1bb1910
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262696021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346044ad945c537b0bbacca887b35def7020e0f1404a6c8d9c238acd6fe4841f`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:44:52 GMT
ENV NEO4J_SHA256=29b854cc540b608d86236102417b7d3d06a027e28eb3d9be8fbf7931f713bca3 NEO4J_TARBALL=neo4j-enterprise-3.5.8-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:44:52 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.8-unix.tar.gz
# Fri, 17 Apr 2020 10:44:54 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.8-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:44:54 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 17 Apr 2020 10:45:15 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.8-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 10:45:15 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:45:15 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:45:16 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:45:16 GMT
COPY file:e07128b8290e38440521f56bbf78b61bbce8be21a97b8b31668594bebdd2bf2b in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:45:17 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:45:17 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:45:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a2c463df21a5a1c26df327f5e3fed04be43142d701c7eca5447230e442bbc0`  
		Last Modified: Fri, 17 Apr 2020 11:01:38 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa8520ec93b271e1b3c4e13c340aab47b49851671f5866db8213ddc9eae62e`  
		Last Modified: Fri, 17 Apr 2020 11:01:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edfd131d964263b9eb6994f428c811abfba9803270f07320b4271bb5496d531`  
		Last Modified: Fri, 17 Apr 2020 11:02:20 GMT  
		Size: 191.7 MB (191749866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2da1b151578006d014d52ca0e9596eba30df03b5d2102a4bab28dd54fbc71`  
		Last Modified: Fri, 17 Apr 2020 11:01:38 GMT  
		Size: 4.3 KB (4348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5-enterprise`

```console
$ docker pull neo4j@sha256:2cc81823dedee03da4d4a33af2eecff9c86ff8a762423745d85bd8bbc8763b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:21ee092f9025d6648b9a5966b588737bd169962c06041730cb9ffa279362f28a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241919044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967769430a35570a48340a2319abe7b3f6c659e85b12829f3bd4e4324c3e4ad3`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 10:38:06 GMT
ENV NEO4J_SHA256=1f8c60e01e8bcdb5c6921341bd4a783c08a748cabb3348d4e4d2f104544232ca NEO4J_TARBALL=neo4j-enterprise-3.5.17-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:38:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
# Fri, 17 Apr 2020 10:38:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:38:09 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:38:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:38:31 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:38:32 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:38:32 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:38:32 GMT
COPY file:cd969a3e3d21f58e9a9a346d321ec15de0b681e0976dc4b74a6a00cb6cd0f32c in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:38:33 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:38:33 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:38:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819d6d2030d11093838d230ecfd42825ddf2ecb6e141d242c88b80c8b8b0598e`  
		Last Modified: Fri, 17 Apr 2020 10:55:41 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e18d3303ad288c4a4315c064fe3eee34d8d2823313e716e0f863f6ca9461da`  
		Last Modified: Fri, 17 Apr 2020 10:55:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0d4827533f72fafef05f4c9232cdfafd235ad5100e5584f18a3d24e088875c`  
		Last Modified: Fri, 17 Apr 2020 10:55:59 GMT  
		Size: 171.0 MB (170971030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce86cc8a14c300a3b29c6bb84dd110d7907af09c87d4e3f698d69451996555c`  
		Last Modified: Fri, 17 Apr 2020 10:55:41 GMT  
		Size: 5.9 KB (5881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0`

```console
$ docker pull neo4j@sha256:7713bbb740800ac7162417eea1d6dc88382863c6d5575be30d5c1e365951e1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0` - linux; amd64

```console
$ docker pull neo4j@sha256:db12a3e5a89a7126dc8f50ab8304a893f6d4ab6a23e3caa996787b496f1e216f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333744338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc9fbb216a070af714e71eb7c0e65aaa5b10176e61e4ed115c583510bebb523`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:34:15 GMT
ENV NEO4J_SHA256=34db8c51899eced35ca5b9ba764649419f160b944b81abc52ed3587492c07085 NEO4J_TARBALL=neo4j-community-4.0.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:34:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
# Fri, 17 Apr 2020 10:34:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:34:18 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:34:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:34:32 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:34:32 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:34:32 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:34:32 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:34:33 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:34:33 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:34:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6356232c5dc126a53bbe910e42b0c15c4c14388538136c471ddfed2ce2ac36b0`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe01e7615c56aecf0f152a8a9584eb721259c82dd64ce03e0deb223a13d6e3`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a1393e04ed0d608f2dfa749f07836ac1c0eb8726adfe3fa4efb63a65af2b1d`  
		Last Modified: Fri, 17 Apr 2020 10:51:56 GMT  
		Size: 106.9 MB (106914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e287dcf41f8aee6993a9a6dddf5d6f81168f462d6a72a17daf8a17afc51ca1ba`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.0`

```console
$ docker pull neo4j@sha256:cc5f731224b905f34965aeffea8c4eeb904df2052a9fd1cd3224354a376116eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.0` - linux; amd64

```console
$ docker pull neo4j@sha256:706c6be67c40d633d577525c323ed5eaa7b76f0ec1945dea0ae3a84aa4603351
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357909746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49805d595336e7b9640af36555cb91d39d769aeacd8b2ecde6a323d42e49fa39`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:36:32 GMT
ENV NEO4J_SHA256=63c85ee709916f9f5fa2fac7274f1a55bdd44d6ab353cbdd05f050aed9532e82 NEO4J_TARBALL=neo4j-community-4.0.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:36:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.0-unix.tar.gz
# Fri, 17 Apr 2020 10:36:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.0-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:36:33 GMT
COPY multi:1bd8b938243645019f0ce38b6c9eeda97edd652b6f36f34befd360fa818b53e9 in /tmp/ 
# Fri, 17 Apr 2020 10:36:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.0-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:36:49 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:36:49 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:36:50 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:36:50 GMT
COPY file:c841ea3ded595df832d5ef9cc6bd4500806b0225676ea4550413353a0f0b82a5 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:36:51 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:36:51 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:36:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66aa235ab704f1f064d3c9999cc50882596ec0618526c950b3668ad7a0618b6`  
		Last Modified: Fri, 17 Apr 2020 10:54:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113d962ed842bb29172e7795195fbc0e7dfa7f8e9e5dc88b76792a18b634fe6f`  
		Last Modified: Fri, 17 Apr 2020 10:54:16 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e00852eaa06b257bd9147b4cc9434134cc4222372edf9afa9b41b174e3d24a`  
		Last Modified: Fri, 17 Apr 2020 10:54:44 GMT  
		Size: 131.1 MB (131079209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1103e601acddc7100440eb382a1c89af99f6b5d07d6c0b7c50273561dde123f`  
		Last Modified: Fri, 17 Apr 2020 10:54:16 GMT  
		Size: 6.1 KB (6075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.0-enterprise`

```console
$ docker pull neo4j@sha256:47441a24a66e2cd5d5788ad51487c266f2d68110846455a04c6757537b322989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:37565ede8d1decc899956c17e98b60e9a887c06f9c4b97e48c6a3843f997ee00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.1 MB (388149678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf19bcb31d13248a26eb6125e4773fd6ef95e82f6fcf7e3de73e9e38c23ff54a`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:36:57 GMT
ENV NEO4J_SHA256=97060ce09086fa089516a2a3581b3db0d3d0dc4d2dd60daa470fa9ba090a7184 NEO4J_TARBALL=neo4j-enterprise-4.0.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:36:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.0-unix.tar.gz
# Fri, 17 Apr 2020 10:37:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.0-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:37:00 GMT
COPY multi:1bd8b938243645019f0ce38b6c9eeda97edd652b6f36f34befd360fa818b53e9 in /tmp/ 
# Fri, 17 Apr 2020 10:37:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.0-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:37:22 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:37:23 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:37:23 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:37:24 GMT
COPY file:c841ea3ded595df832d5ef9cc6bd4500806b0225676ea4550413353a0f0b82a5 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:37:24 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:37:24 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:37:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baa425948a1902550feddc9c56454c2e69d5ef3e7f8a21c116ddc55b37caccb`  
		Last Modified: Fri, 17 Apr 2020 10:54:48 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba914fac4c2c0740a1fb12d39595eb0cd78705fcfd23f498cea97b6bb6fc3f73`  
		Last Modified: Fri, 17 Apr 2020 10:54:48 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141fdd15be1a8c889358cc5fec1a5ddd45a847ccc3956a7b288de1dbd453bf3f`  
		Last Modified: Fri, 17 Apr 2020 10:55:12 GMT  
		Size: 161.3 MB (161319138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038cb435e97cb3284a93741f39cde0a4c93224c02d034d66816e97339fbd213a`  
		Last Modified: Fri, 17 Apr 2020 10:54:48 GMT  
		Size: 6.1 KB (6075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.1`

```console
$ docker pull neo4j@sha256:b9ced06ca43a8d1a5fe09849000581974fc851d69f139a02311699c2ee1b9d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.1` - linux; amd64

```console
$ docker pull neo4j@sha256:7601f98039490f02dacebee9319a7d6cd9decaa2fdbd5c07128f48b7b7f0c8cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.6 MB (333649371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60152975f5fc792707811eda2168f02a653b5764609d5b3a0591e2da37922074`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:35:48 GMT
ENV NEO4J_SHA256=623c807ec23ed5c5e8db665a36bcdcb03a11ca2179ce24b61b220ecac60ace90 NEO4J_TARBALL=neo4j-community-4.0.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:35:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.1-unix.tar.gz
# Fri, 17 Apr 2020 10:35:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.1-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:35:50 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:36:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.1-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:36:03 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:36:04 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:36:04 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:36:04 GMT
COPY file:180882cf912cbd895c07318211915dd64e94178cf2bd8093fdaf8e8c1b4692f3 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:36:04 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:36:05 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:36:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbf086136720693a9ce9e0fe3b9aa56dabc72b42dc6eca91f5d0af746358746`  
		Last Modified: Fri, 17 Apr 2020 10:53:36 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa177af1ae232907132b06769bda79f11509c79de66881acae6533fab6f882d`  
		Last Modified: Fri, 17 Apr 2020 10:53:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211eec15ee219fd8dd1721f394f7888d065edeb7cb187709732c198e6b55fdb8`  
		Last Modified: Fri, 17 Apr 2020 10:53:51 GMT  
		Size: 106.8 MB (106818792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25da26c975954f8dc2c5e38ab57a1388ad5dced5b1a0997ca34154c34991eb4f`  
		Last Modified: Fri, 17 Apr 2020 10:53:36 GMT  
		Size: 6.1 KB (6085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.1-enterprise`

```console
$ docker pull neo4j@sha256:5b73ee9085ba94f9b657bd31e07eb98d188367cb78d7b57fa9f8351bb4d504dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2f5db899398693f619e2dc3392b450cfb5770fed57b14a4f3246f31240ed10a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363926666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea70ff1e035c102cfaadc39015a378dc49df0c2ca6d4c49de09015e58e7595c`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:36:10 GMT
ENV NEO4J_SHA256=8c6aed4f05246a494ca5ec282f8fd7b4d8342c55adfd3dfa474b4e474f19fe09 NEO4J_TARBALL=neo4j-enterprise-4.0.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:36:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.1-unix.tar.gz
# Fri, 17 Apr 2020 10:36:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.1-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:36:11 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:36:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.1-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:36:26 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:36:27 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:36:27 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:36:27 GMT
COPY file:180882cf912cbd895c07318211915dd64e94178cf2bd8093fdaf8e8c1b4692f3 in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:36:27 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:36:27 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:36:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1426392b60e2557d95f589ac7d0cd83193bf604496f3d412e18f9065386e0de`  
		Last Modified: Fri, 17 Apr 2020 10:53:56 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7963775f25839754e860ef867c38345ab09f48b817c39bc96d36f048ff4569f`  
		Last Modified: Fri, 17 Apr 2020 10:53:56 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef164b7e42590059019b6de4815561d6279f6d96870719906387c593e0041e0`  
		Last Modified: Fri, 17 Apr 2020 10:54:12 GMT  
		Size: 137.1 MB (137096088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e43a2fb708c11c4b48736d58d3e29261e9f57d3e37682b2bfd50cb844ea53`  
		Last Modified: Fri, 17 Apr 2020 10:53:56 GMT  
		Size: 6.1 KB (6085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.2`

```console
$ docker pull neo4j@sha256:1a64817cbcab0ea1187c402033198c20c61e1185509ef7426fb3d539a2fa9001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.2` - linux; amd64

```console
$ docker pull neo4j@sha256:a44e6bda69dae98675f796dfe30ca840089c6b44ce304f307e16ef14045ce372
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333694520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c7e3b60d9d09b655c8a7ac1f41d0236f664ac8ebcbb722d1ba1b4eae61f1cd`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:35:02 GMT
ENV NEO4J_SHA256=e189f557a41835170fae42ee8d2dea9a94a3c790cfc73f0d9eb28be21b806830 NEO4J_TARBALL=neo4j-community-4.0.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:35:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.2-unix.tar.gz
# Fri, 17 Apr 2020 10:35:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.2-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:35:03 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:35:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.2-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:35:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:35:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:35:18 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:35:18 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:35:18 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:35:19 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:35:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11995cea54e582e7ce8260d5aec26c519b78fcd5aaa0da77c42545d2046103e5`  
		Last Modified: Fri, 17 Apr 2020 10:52:45 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e81d385917b605e1882bfbd742332876fe9ddf96716677f8a572f91284c24b`  
		Last Modified: Fri, 17 Apr 2020 10:52:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418bccccc1be5df6f0f0378017ee2ab2fd777172a59a9edd7c8b0ea692a23a70`  
		Last Modified: Fri, 17 Apr 2020 10:53:01 GMT  
		Size: 106.9 MB (106864186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ff865ba0f1f6a7f3e22729609c1cb6804bf7bf76c0d9abbe40d11a57d9d850`  
		Last Modified: Fri, 17 Apr 2020 10:52:45 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.2-enterprise`

```console
$ docker pull neo4j@sha256:a1cd1a355c2bc4ad0538cd8477d82e79479676341ecb6522f75a822edeeb0908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.2-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b1f75786bf63555258b8f902dcc593115104d4ae61f9a9f60d53fa5b96d41443
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (363993118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe18467f026bc521ea416de4a942216daff750d7418f93ecb91fdfd1fff6c82`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:35:23 GMT
ENV NEO4J_SHA256=a39791336692e0cabb06f725b9f76dda43c80ef0d8073d696fea8feb5ee502f4 NEO4J_TARBALL=neo4j-enterprise-4.0.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:35:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.2-unix.tar.gz
# Fri, 17 Apr 2020 10:35:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.2-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:35:25 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:35:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.2-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:35:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:35:40 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:35:41 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:35:41 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:35:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:35:41 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:35:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95847fdcf8702673b8d9ff4bf7c318625860736343006ea76b677bf69cbcec85`  
		Last Modified: Fri, 17 Apr 2020 10:53:05 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa001a4c56598efd319edbb241d0a694cfacfb98f12ea66eccd98e86624c016`  
		Last Modified: Fri, 17 Apr 2020 10:53:05 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d827b4543410b0d7ad69c3507b1cdfbf9547e492687b2cb66ecd6880984bc1`  
		Last Modified: Fri, 17 Apr 2020 10:53:32 GMT  
		Size: 137.2 MB (137162790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236441da1205f429eb7a74a4ed46236506a8dd507cbe636c1bd9a016bdd36535`  
		Last Modified: Fri, 17 Apr 2020 10:53:05 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.3`

```console
$ docker pull neo4j@sha256:7713bbb740800ac7162417eea1d6dc88382863c6d5575be30d5c1e365951e1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.3` - linux; amd64

```console
$ docker pull neo4j@sha256:db12a3e5a89a7126dc8f50ab8304a893f6d4ab6a23e3caa996787b496f1e216f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333744338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc9fbb216a070af714e71eb7c0e65aaa5b10176e61e4ed115c583510bebb523`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:34:15 GMT
ENV NEO4J_SHA256=34db8c51899eced35ca5b9ba764649419f160b944b81abc52ed3587492c07085 NEO4J_TARBALL=neo4j-community-4.0.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:34:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
# Fri, 17 Apr 2020 10:34:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:34:18 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:34:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:34:32 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:34:32 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:34:32 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:34:32 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:34:33 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:34:33 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:34:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6356232c5dc126a53bbe910e42b0c15c4c14388538136c471ddfed2ce2ac36b0`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe01e7615c56aecf0f152a8a9584eb721259c82dd64ce03e0deb223a13d6e3`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a1393e04ed0d608f2dfa749f07836ac1c0eb8726adfe3fa4efb63a65af2b1d`  
		Last Modified: Fri, 17 Apr 2020 10:51:56 GMT  
		Size: 106.9 MB (106914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e287dcf41f8aee6993a9a6dddf5d6f81168f462d6a72a17daf8a17afc51ca1ba`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.3-enterprise`

```console
$ docker pull neo4j@sha256:4e2d46532614765013ca9a5131e1eb0b8af2d2387d6824b7049767eab07d25c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2d9719c327f3a26e450dca41d710456af6c908eb97c6a5077b17baa3a43e6bc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (364045495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5cc9df763a837ef21c245fec8fac8ca4e7ae8f88f8e12639333e8e173c5698`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:34:37 GMT
ENV NEO4J_SHA256=f70ea236b75d4210a49ff4e009388cc99577d50a38eb25ac73fce16eee783aa0 NEO4J_TARBALL=neo4j-enterprise-4.0.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:34:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
# Fri, 17 Apr 2020 10:34:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:34:38 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:34:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:34:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:34:55 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:34:55 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:34:56 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:34:56 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:34:56 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:34:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87b6896625d4650c698007c0552481df952ab3763c3bc52716ccc5ae9f658b6`  
		Last Modified: Fri, 17 Apr 2020 10:52:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be9cc5c5998057b2af0ecedcba74dd74b7cf6a3d3227a334332234f65463a53`  
		Last Modified: Fri, 17 Apr 2020 10:52:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca562146b152109c0e2836b080cb15b2488b560dfd0f7da42cd0b86b1bef93ed`  
		Last Modified: Fri, 17 Apr 2020 10:52:40 GMT  
		Size: 137.2 MB (137215167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00df00c172f8389585044aaa761f3f67005040e93c99e4a5c13e24f4377bc9b7`  
		Last Modified: Fri, 17 Apr 2020 10:52:01 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0-enterprise`

```console
$ docker pull neo4j@sha256:4e2d46532614765013ca9a5131e1eb0b8af2d2387d6824b7049767eab07d25c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2d9719c327f3a26e450dca41d710456af6c908eb97c6a5077b17baa3a43e6bc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (364045495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5cc9df763a837ef21c245fec8fac8ca4e7ae8f88f8e12639333e8e173c5698`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:34:37 GMT
ENV NEO4J_SHA256=f70ea236b75d4210a49ff4e009388cc99577d50a38eb25ac73fce16eee783aa0 NEO4J_TARBALL=neo4j-enterprise-4.0.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:34:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
# Fri, 17 Apr 2020 10:34:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:34:38 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:34:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:34:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:34:55 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:34:55 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:34:56 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:34:56 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:34:56 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:34:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87b6896625d4650c698007c0552481df952ab3763c3bc52716ccc5ae9f658b6`  
		Last Modified: Fri, 17 Apr 2020 10:52:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be9cc5c5998057b2af0ecedcba74dd74b7cf6a3d3227a334332234f65463a53`  
		Last Modified: Fri, 17 Apr 2020 10:52:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca562146b152109c0e2836b080cb15b2488b560dfd0f7da42cd0b86b1bef93ed`  
		Last Modified: Fri, 17 Apr 2020 10:52:40 GMT  
		Size: 137.2 MB (137215167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00df00c172f8389585044aaa761f3f67005040e93c99e4a5c13e24f4377bc9b7`  
		Last Modified: Fri, 17 Apr 2020 10:52:01 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:4e2d46532614765013ca9a5131e1eb0b8af2d2387d6824b7049767eab07d25c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2d9719c327f3a26e450dca41d710456af6c908eb97c6a5077b17baa3a43e6bc3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (364045495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5cc9df763a837ef21c245fec8fac8ca4e7ae8f88f8e12639333e8e173c5698`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:34:37 GMT
ENV NEO4J_SHA256=f70ea236b75d4210a49ff4e009388cc99577d50a38eb25ac73fce16eee783aa0 NEO4J_TARBALL=neo4j-enterprise-4.0.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:34:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
# Fri, 17 Apr 2020 10:34:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:34:38 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:34:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:34:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:34:55 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:34:55 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:34:56 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:34:56 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:34:56 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:34:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87b6896625d4650c698007c0552481df952ab3763c3bc52716ccc5ae9f658b6`  
		Last Modified: Fri, 17 Apr 2020 10:52:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be9cc5c5998057b2af0ecedcba74dd74b7cf6a3d3227a334332234f65463a53`  
		Last Modified: Fri, 17 Apr 2020 10:52:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca562146b152109c0e2836b080cb15b2488b560dfd0f7da42cd0b86b1bef93ed`  
		Last Modified: Fri, 17 Apr 2020 10:52:40 GMT  
		Size: 137.2 MB (137215167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00df00c172f8389585044aaa761f3f67005040e93c99e4a5c13e24f4377bc9b7`  
		Last Modified: Fri, 17 Apr 2020 10:52:01 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:7713bbb740800ac7162417eea1d6dc88382863c6d5575be30d5c1e365951e1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:db12a3e5a89a7126dc8f50ab8304a893f6d4ab6a23e3caa996787b496f1e216f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333744338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc9fbb216a070af714e71eb7c0e65aaa5b10176e61e4ed115c583510bebb523`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Thu, 16 Apr 2020 10:19:15 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:19:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Thu, 16 Apr 2020 10:19:37 GMT
CMD ["jshell"]
# Fri, 17 Apr 2020 10:34:15 GMT
ENV NEO4J_SHA256=34db8c51899eced35ca5b9ba764649419f160b944b81abc52ed3587492c07085 NEO4J_TARBALL=neo4j-community-4.0.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 17 Apr 2020 10:34:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
# Fri, 17 Apr 2020 10:34:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Apr 2020 10:34:18 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 17 Apr 2020 10:34:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 17 Apr 2020 10:34:32 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 10:34:32 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Apr 2020 10:34:32 GMT
VOLUME [/data /logs]
# Fri, 17 Apr 2020 10:34:32 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Fri, 17 Apr 2020 10:34:33 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Apr 2020 10:34:33 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Apr 2020 10:34:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70d371bf7f48019cf4226aa265f7912867d542cd9f3c3ec6ae43ac7ade65731`  
		Last Modified: Thu, 16 Apr 2020 10:27:08 GMT  
		Size: 196.5 MB (196475178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6356232c5dc126a53bbe910e42b0c15c4c14388538136c471ddfed2ce2ac36b0`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe01e7615c56aecf0f152a8a9584eb721259c82dd64ce03e0deb223a13d6e3`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a1393e04ed0d608f2dfa749f07836ac1c0eb8726adfe3fa4efb63a65af2b1d`  
		Last Modified: Fri, 17 Apr 2020 10:51:56 GMT  
		Size: 106.9 MB (106914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e287dcf41f8aee6993a9a6dddf5d6f81168f462d6a72a17daf8a17afc51ca1ba`  
		Last Modified: Fri, 17 Apr 2020 10:51:45 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
