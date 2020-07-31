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
-	[`neo4j:3.4.18`](#neo4j3418)
-	[`neo4j:3.4.18-enterprise`](#neo4j3418-enterprise)
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
-	[`neo4j:3.5.18`](#neo4j3518)
-	[`neo4j:3.5.18-enterprise`](#neo4j3518-enterprise)
-	[`neo4j:3.5.19`](#neo4j3519)
-	[`neo4j:3.5.19-enterprise`](#neo4j3519-enterprise)
-	[`neo4j:3.5.20`](#neo4j3520)
-	[`neo4j:3.5.20-enterprise`](#neo4j3520-enterprise)
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
-	[`neo4j:4.0.4`](#neo4j404)
-	[`neo4j:4.0.4-enterprise`](#neo4j404-enterprise)
-	[`neo4j:4.0.5`](#neo4j405)
-	[`neo4j:4.0.5-enterprise`](#neo4j405-enterprise)
-	[`neo4j:4.0.6`](#neo4j406)
-	[`neo4j:4.0.6-enterprise`](#neo4j406-enterprise)
-	[`neo4j:4.0.7`](#neo4j407)
-	[`neo4j:4.0.7-enterprise`](#neo4j407-enterprise)
-	[`neo4j:4.0-enterprise`](#neo4j40-enterprise)
-	[`neo4j:4.1`](#neo4j41)
-	[`neo4j:4.1.0`](#neo4j410)
-	[`neo4j:4.1.0-enterprise`](#neo4j410-enterprise)
-	[`neo4j:4.1.1`](#neo4j411)
-	[`neo4j:4.1.1-enterprise`](#neo4j411-enterprise)
-	[`neo4j:4.1-enterprise`](#neo4j41-enterprise)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:3.4`

```console
$ docker pull neo4j@sha256:f0998ae5485ab6d65116e804ae949e04689bfe41b45ae97ade1c37355f9ff32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4` - linux; amd64

```console
$ docker pull neo4j@sha256:0ef5b9d754f6f9dfa601723572f7d31dfc155fcac9f409732d8dca2029ef6956
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190240028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8072ac30a88679e4b9a5dfeb4a6e38126bd5efb04f61f5ddb359e71910a69fe`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:06:49 GMT
ENV NEO4J_SHA256=c9f9f8458d65e42fb92c788c85e79882cf307f18bd0f36fbeb2a76162ed6535b NEO4J_TARBALL=neo4j-community-3.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:06:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.18-unix.tar.gz
# Fri, 31 Jul 2020 00:06:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.18-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:06:51 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Fri, 31 Jul 2020 00:07:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.18-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:07:03 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:07:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:07:03 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:07:04 GMT
COPY file:a2648bdbd872a646c12deefe05a5ae67873d2050cb12d7befc550380f89b8b8e in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:07:04 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:07:04 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:07:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8958429d14c5a2920b5d23cfc0affb0c24595e315e6a64765e82b70b519c4801`  
		Last Modified: Fri, 31 Jul 2020 00:18:46 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f0af7a82d9266d205dbcb83eb7505d4293614ec08b72bd57abb882329cd08`  
		Last Modified: Fri, 31 Jul 2020 00:18:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfe3ee7eba0fd6bbdce773d572b6e351c566f2f46b876f085479a06008fcff2`  
		Last Modified: Fri, 31 Jul 2020 00:18:54 GMT  
		Size: 119.3 MB (119274821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8a0c73084822f7a575d21c5586893c4a4af6d2a916edc3ac32176e85d6eb60`  
		Last Modified: Fri, 31 Jul 2020 00:18:45 GMT  
		Size: 5.9 KB (5890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.14`

```console
$ docker pull neo4j@sha256:2d5ea8677a33155d4897e22980d4a6e2022d354ff6d5f63e0dd714b0c2d1883f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.14` - linux; amd64

```console
$ docker pull neo4j@sha256:51f2ef0cf43deffeac1aefb67ae717051fddf5b5f24c22af3fde9a6834b34f0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225617759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ff4eb134c4d4a3b720d01e68530b6612aef6417eba4a1fcbecf3c148d1331`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:09:55 GMT
ENV NEO4J_SHA256=fcbdd7abc28a50cca76daed96d60a6d7d03a4db5bbbfdfb8e520ee1984698461 NEO4J_TARBALL=neo4j-community-3.4.14-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:09:55 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.14-unix.tar.gz
# Fri, 31 Jul 2020 00:09:57 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.14-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:09:57 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:10:13 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.14-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 31 Jul 2020 00:10:13 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:10:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:10:14 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:10:14 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:10:14 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:10:14 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:10:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70196238d18efe1f063810a6f7d1d2450b47651fdb68a8040e9fbb437cb5cb20`  
		Last Modified: Fri, 31 Jul 2020 00:20:57 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c1f635fa0f973120e53d31586f594b2e4ff19b86f25956517f79410160a84`  
		Last Modified: Fri, 31 Jul 2020 00:20:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121a02c3aa3314f947563003ce3a1dc605496f1a47bd77eb64ad1a9c87b07416`  
		Last Modified: Fri, 31 Jul 2020 00:21:07 GMT  
		Size: 154.7 MB (154654424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4029f013a184e43d4581ea0b32b8cc13649eecabc44b8ebff19cc8a4bcf4c536`  
		Last Modified: Fri, 31 Jul 2020 00:20:57 GMT  
		Size: 4.4 KB (4386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.14-enterprise`

```console
$ docker pull neo4j@sha256:de84d9280e94c75f32c15ea900fda1cc5bb102e7488b92da058f2d860e947740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.14-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ff193eb97e8183d5ad55d0aa7f08ac4659f5fd321cbb29e7d0247b2c84f9b274
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242401213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4057f00caf6fad03afad74ed173ee87062343e9827fd0817eddca8ce3bb58809`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:10:20 GMT
ENV NEO4J_SHA256=5ebd47769a7aa25343d0b1ea59c2e9f2c847c56ac344ce2644d1f60496a7386f NEO4J_TARBALL=neo4j-enterprise-3.4.14-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:10:20 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.14-unix.tar.gz
# Fri, 31 Jul 2020 00:10:21 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.14-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:10:22 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:10:39 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.14-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 31 Jul 2020 00:10:39 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:10:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:10:40 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:10:40 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:10:40 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:10:40 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:10:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d4b034fc4e887f33377b0c4a953a90ca611e39bf3ed75ddbf2453359142618`  
		Last Modified: Fri, 31 Jul 2020 00:21:11 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc58cefb75fa1abfd6545f7196104a45f01bb52a652126f91750316b164209e0`  
		Last Modified: Fri, 31 Jul 2020 00:21:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44d6165a9a3c068fba6e907f4a1d0dc896ce58da3da63a2df27c18f7a7dbf7`  
		Last Modified: Fri, 31 Jul 2020 00:21:24 GMT  
		Size: 171.4 MB (171437883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb49bcfe150d3e286c41d9bd207f2c82a6bc5c0c8fb2e3b28cd982811ffe6bb`  
		Last Modified: Fri, 31 Jul 2020 00:21:12 GMT  
		Size: 4.4 KB (4386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.15`

```console
$ docker pull neo4j@sha256:16b027e6732b4b12bde48bce5f56bc5ca7d16cbc8baef64cabf2e572d4f89630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.15` - linux; amd64

```console
$ docker pull neo4j@sha256:29fd6ab2beb576b02d00cd9c13373848ed6a49ae680c71f8a57c0aa62b0f3007
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212182279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8148aa3675c683a60c862d6463685418270ceffad69507349056046442e9ed31`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:09:08 GMT
ENV NEO4J_SHA256=7e230753e2c53c912829f1ed2df963fbacc3892acd3501a84892118317fbccda NEO4J_TARBALL=neo4j-community-3.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:09:08 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.15-unix.tar.gz
# Fri, 31 Jul 2020 00:09:09 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.15-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:09:09 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:09:24 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:09:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:09:25 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:09:25 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:09:25 GMT
COPY file:e07128b8290e38440521f56bbf78b61bbce8be21a97b8b31668594bebdd2bf2b in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:09:25 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:09:26 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:09:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a3a2d14d36bd67739e1da30f1e5ba9e4d562e3a7e8f1960e64fafd007565c0`  
		Last Modified: Fri, 31 Jul 2020 00:20:26 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7dfbf10990cb8c7339c56ee3b11ca61ad72d35d0f75f483fbc14483e6a9f9f`  
		Last Modified: Fri, 31 Jul 2020 00:20:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefc7b4d5750ab530ddf9f02a3a4e7750eb567a1ff80a86ec7a960bf191e7320`  
		Last Modified: Fri, 31 Jul 2020 00:20:36 GMT  
		Size: 141.2 MB (141218986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0970a081a247d0b965bcc0485db0d860eb48a0c621d2d24c2051922c225de57`  
		Last Modified: Fri, 31 Jul 2020 00:20:26 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.15-enterprise`

```console
$ docker pull neo4j@sha256:97e91c9dcf5855ba76c2d8340d0616495d8a0ac8b134e7e8841fae73e37ec9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:4bcde6c9d60a91021237d45d407b146648a95e94484965cb965a6e5f70d3f122
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228964737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8be658c7e06d52bb70d14b9f3d78a96f34372ad6b57b24ce2fea53416a3d6`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:09:29 GMT
ENV NEO4J_SHA256=d7d215dcdbb9e5d6bb426003d62a1be2ffe3cb20039bb3432be8f9eab9be9e56 NEO4J_TARBALL=neo4j-enterprise-3.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:09:30 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.15-unix.tar.gz
# Fri, 31 Jul 2020 00:09:30 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.15-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:09:31 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:09:47 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:09:47 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:09:47 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:09:48 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:09:48 GMT
COPY file:e07128b8290e38440521f56bbf78b61bbce8be21a97b8b31668594bebdd2bf2b in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:09:48 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:09:48 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:09:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8768fbcd2580a0037ec94715d104a00375bc0f956e126f0ae0e65c33f67638fe`  
		Last Modified: Fri, 31 Jul 2020 00:20:41 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02eafb65b6cb39efdaccfd262c44e6518f80577f7a737be6de84b16644457635`  
		Last Modified: Fri, 31 Jul 2020 00:20:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360d340c1df33983b2b7faee25393508b80428aad2fdc47d368f0757273ae30`  
		Last Modified: Fri, 31 Jul 2020 00:20:52 GMT  
		Size: 158.0 MB (158001445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206906064576780f2ff374d2177bf7cde3548b4cf604b67a562ed754d46be931`  
		Last Modified: Fri, 31 Jul 2020 00:20:41 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.16`

```console
$ docker pull neo4j@sha256:c6989c44091e81aec2514ee2a0ec3a0b572df16ac0f5564552b49a6af5025210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.16` - linux; amd64

```console
$ docker pull neo4j@sha256:21a22572ad166daa84ecd2a085907a53acf8199925505393c0ca870c01cabb47
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212644840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2be01fa62e4ce6908f4c85e7e01eb4e278550f970fed5e32a01799cc6c3f026`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:08:21 GMT
ENV NEO4J_SHA256=8c42ebe3455d92deedb09417dc02bcd37f5e0f13eb3f3faa5f1a5b9d4a781c7b NEO4J_TARBALL=neo4j-community-3.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:08:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.16-unix.tar.gz
# Fri, 31 Jul 2020 00:08:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.16-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:08:22 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:08:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:08:37 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:08:37 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:08:38 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:08:38 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:08:38 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:08:38 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:08:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898c3e9c9872848f1be1f9dbe286af3474065d36169f8595903c3a14f5ffd111`  
		Last Modified: Fri, 31 Jul 2020 00:19:56 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbfb6727f980e2df2ac718e95f33a76badb97821c755e26ffa4bab07df734fb`  
		Last Modified: Fri, 31 Jul 2020 00:19:56 GMT  
		Size: 301.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd171b0ddd878ca20660d31007acd24c81fcf3e9209ff011dc1a2afcf5a94861`  
		Last Modified: Fri, 31 Jul 2020 00:20:06 GMT  
		Size: 141.7 MB (141680419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52a4c067cb3715a34a4f7800101970ce6f16a0e613a348b0a5e9b51bc323248`  
		Last Modified: Fri, 31 Jul 2020 00:19:56 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.16-enterprise`

```console
$ docker pull neo4j@sha256:2d5283272b0c9558770e407f155b151783a84ab88a1427dd69e39ed206649cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:daa630f35dccac55df71c89f54cbd4b27772ab6da1d359fe7766f528dc57a5ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229426856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5319c23acec07b9854fb373f2e26e29cabdcdfe8161d2a2e9b29c28f71586ca6`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:08:43 GMT
ENV NEO4J_SHA256=ba8cf11ba8eb689755fcb7aacedf74391c6b5ec9ff423e921948ace401db12b9 NEO4J_TARBALL=neo4j-enterprise-3.4.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:08:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.16-unix.tar.gz
# Fri, 31 Jul 2020 00:08:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.16-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:08:44 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:09:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:09:00 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:09:01 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:09:01 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:09:01 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:09:01 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:09:01 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:09:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fb963daa3ba1bedeb4de42786050194671eddae913af31b6d749806dab2388`  
		Last Modified: Fri, 31 Jul 2020 00:20:11 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2963ee0076e4e0911a445fa574c72a48dc5f118649c06bca0b9af43bddfe22`  
		Last Modified: Fri, 31 Jul 2020 00:20:11 GMT  
		Size: 301.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86366cabe7533f3b94cc932bde2bc18c57537a42901a9085f67841dc8cdbbe4b`  
		Last Modified: Fri, 31 Jul 2020 00:20:22 GMT  
		Size: 158.5 MB (158462435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b402e628dc9a0c8832db8acf7de4f2df0c48c278b8276b952476be5065b9146e`  
		Last Modified: Fri, 31 Jul 2020 00:20:11 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.17`

```console
$ docker pull neo4j@sha256:ebb28eb55d394932198a3c1d00fb1eb6658872375d253a03bcbac4cc78c254af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.17` - linux; amd64

```console
$ docker pull neo4j@sha256:eb0220cad9310b7fe46d6f49d1f22ee3a5a4dd44402d1f1007bf3e32fc7abb4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8128510d03d2539f87d6a7fac36f2170317209413946de9fefb67e58c6fbbce`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:07:34 GMT
ENV NEO4J_SHA256=fbb03e85a09e1e8a77c496ad61e8094ef94185268098634a4aaf1d1a01b841a6 NEO4J_TARBALL=neo4j-community-3.4.17-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:07:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
# Fri, 31 Jul 2020 00:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:07:35 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:07:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:07:50 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:07:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:07:50 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:07:51 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:07:51 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:07:51 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:07:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150b71485540c201391dda7515c32553b93a685bb62cb81ac06245658e2ac509`  
		Last Modified: Fri, 31 Jul 2020 00:19:27 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8660e840c7cb3446dda8ab79da30dc32526594a7e50af8f058e64ddd6516bb8`  
		Last Modified: Fri, 31 Jul 2020 00:19:27 GMT  
		Size: 301.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9766a6d67bcc9a30cb2076519d763675763e75b6002cf3ea03a0248948557fe5`  
		Last Modified: Fri, 31 Jul 2020 00:19:37 GMT  
		Size: 144.1 MB (144082268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb215cd2110ef9841e8442576f11082effec14e8393505b93b2fab7ef36b52f2`  
		Last Modified: Fri, 31 Jul 2020 00:19:28 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.17-enterprise`

```console
$ docker pull neo4j@sha256:943836a0af20b187d1ce18af3daf764e2427d2eefda330587f595459134f4959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.17-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fe438f6e12ed1bbdacbac8a571a53c3c022bf4ca5234108bdcda4da115514107
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231830017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb5bddd6698d9355457ed44367d1fef82947d00abc70b89223a395e2f0fae3c`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:07:56 GMT
ENV NEO4J_SHA256=7d8d689ddc605c66296fadedb0d6810b8159513cb596b68b730f2604ce8bb9df NEO4J_TARBALL=neo4j-enterprise-3.4.17-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:07:56 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
# Fri, 31 Jul 2020 00:07:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:07:57 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:08:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.17-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:08:15 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:08:15 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:08:15 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:08:15 GMT
COPY file:d76df40f02e9ebf317a807eaee3b8b30c3997b4bca927f8a336e347e3901f7b6 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:08:15 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:08:15 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:08:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8c77b31c6b096f6dbe88728a38f7a83cdd5258018584fc84a88ebc65627f9d`  
		Last Modified: Fri, 31 Jul 2020 00:19:41 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab6200d0dde581af71ed17a9c33bfbac5aaf906ed7ed19b21c7af6f6fad57bb`  
		Last Modified: Fri, 31 Jul 2020 00:19:41 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fa1f1277923fe80eaa217b32bd2c715c177b7af7ef278ea4596b8c08f46bf0`  
		Last Modified: Fri, 31 Jul 2020 00:19:53 GMT  
		Size: 160.9 MB (160865595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf0001be086abebd4a8e55991f9e6311b442e0ecf0e6f017e71e4d735a4e86`  
		Last Modified: Fri, 31 Jul 2020 00:19:41 GMT  
		Size: 5.3 KB (5302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.18`

```console
$ docker pull neo4j@sha256:f0998ae5485ab6d65116e804ae949e04689bfe41b45ae97ade1c37355f9ff32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.18` - linux; amd64

```console
$ docker pull neo4j@sha256:0ef5b9d754f6f9dfa601723572f7d31dfc155fcac9f409732d8dca2029ef6956
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190240028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8072ac30a88679e4b9a5dfeb4a6e38126bd5efb04f61f5ddb359e71910a69fe`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:06:49 GMT
ENV NEO4J_SHA256=c9f9f8458d65e42fb92c788c85e79882cf307f18bd0f36fbeb2a76162ed6535b NEO4J_TARBALL=neo4j-community-3.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:06:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.18-unix.tar.gz
# Fri, 31 Jul 2020 00:06:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.18-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:06:51 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Fri, 31 Jul 2020 00:07:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.4.18-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:07:03 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:07:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:07:03 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:07:04 GMT
COPY file:a2648bdbd872a646c12deefe05a5ae67873d2050cb12d7befc550380f89b8b8e in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:07:04 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:07:04 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:07:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8958429d14c5a2920b5d23cfc0affb0c24595e315e6a64765e82b70b519c4801`  
		Last Modified: Fri, 31 Jul 2020 00:18:46 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f0af7a82d9266d205dbcb83eb7505d4293614ec08b72bd57abb882329cd08`  
		Last Modified: Fri, 31 Jul 2020 00:18:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfe3ee7eba0fd6bbdce773d572b6e351c566f2f46b876f085479a06008fcff2`  
		Last Modified: Fri, 31 Jul 2020 00:18:54 GMT  
		Size: 119.3 MB (119274821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8a0c73084822f7a575d21c5586893c4a4af6d2a916edc3ac32176e85d6eb60`  
		Last Modified: Fri, 31 Jul 2020 00:18:45 GMT  
		Size: 5.9 KB (5890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4.18-enterprise`

```console
$ docker pull neo4j@sha256:0384394b99a8dcd98b66023007c0ea4f645f89fcc4811fd559d823556e5d2784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4.18-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d493e3c663170bf34744a2fbc9f8991ac9ce522291d458943b579126a060d28a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (207028007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301cf513df0d283de97514b049f962079eac8cc289c9e8076d10a2c4717b4b04`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:07:08 GMT
ENV NEO4J_SHA256=19226a8a4bb7f3646c61cb366c31d761f43489efb1d96b0bb257dc32b9676af1 NEO4J_TARBALL=neo4j-enterprise-3.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:07:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.18-unix.tar.gz
# Fri, 31 Jul 2020 00:07:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.18-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:07:10 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Fri, 31 Jul 2020 00:07:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.18-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:07:27 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:07:27 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:07:27 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:07:27 GMT
COPY file:a2648bdbd872a646c12deefe05a5ae67873d2050cb12d7befc550380f89b8b8e in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:07:28 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:07:28 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:07:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2538f69f32a74d05596544871458df5866de91502bc5c81dff60829650e8589`  
		Last Modified: Fri, 31 Jul 2020 00:18:58 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee4eacc304637e6d041c52f95b9d985b5149ae6104a10c053473d9ae4269eb1`  
		Last Modified: Fri, 31 Jul 2020 00:18:59 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1dda16cc56131c9a0ee9fcbd4241bf637d94e9e4a95bc75e44077781dfc5ff`  
		Last Modified: Fri, 31 Jul 2020 00:19:22 GMT  
		Size: 136.1 MB (136062800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed0e9808a6432879b7178cce40869604f4ef18a057092a323fedbcccec232f3`  
		Last Modified: Fri, 31 Jul 2020 00:18:58 GMT  
		Size: 5.9 KB (5891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.4-enterprise`

```console
$ docker pull neo4j@sha256:0384394b99a8dcd98b66023007c0ea4f645f89fcc4811fd559d823556e5d2784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d493e3c663170bf34744a2fbc9f8991ac9ce522291d458943b579126a060d28a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (207028007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301cf513df0d283de97514b049f962079eac8cc289c9e8076d10a2c4717b4b04`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:07:08 GMT
ENV NEO4J_SHA256=19226a8a4bb7f3646c61cb366c31d761f43489efb1d96b0bb257dc32b9676af1 NEO4J_TARBALL=neo4j-enterprise-3.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:07:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.18-unix.tar.gz
# Fri, 31 Jul 2020 00:07:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.18-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:07:10 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Fri, 31 Jul 2020 00:07:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.4.18-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:07:27 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:07:27 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:07:27 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:07:27 GMT
COPY file:a2648bdbd872a646c12deefe05a5ae67873d2050cb12d7befc550380f89b8b8e in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:07:28 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:07:28 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:07:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2538f69f32a74d05596544871458df5866de91502bc5c81dff60829650e8589`  
		Last Modified: Fri, 31 Jul 2020 00:18:58 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee4eacc304637e6d041c52f95b9d985b5149ae6104a10c053473d9ae4269eb1`  
		Last Modified: Fri, 31 Jul 2020 00:18:59 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1dda16cc56131c9a0ee9fcbd4241bf637d94e9e4a95bc75e44077781dfc5ff`  
		Last Modified: Fri, 31 Jul 2020 00:19:22 GMT  
		Size: 136.1 MB (136062800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed0e9808a6432879b7178cce40869604f4ef18a057092a323fedbcccec232f3`  
		Last Modified: Fri, 31 Jul 2020 00:18:58 GMT  
		Size: 5.9 KB (5891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5`

```console
$ docker pull neo4j@sha256:677cb9e83988bb0947ceedf9183ade957cd550adaab187c23f208b2c6d343e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5` - linux; amd64

```console
$ docker pull neo4j@sha256:37e8c844c117e0bf413293b6c2ba843ccf3207d3dbcb10cb8d2de474082685a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207964606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84698499aef66b7a5bdd7beb69b0a0171efb9f2f8c20cfa5a80fd3f756527be`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:56:01 GMT
ENV NEO4J_SHA256=01406d4e6a9e89340637aac779adb189db9af66e9c615804ad1ccc17346c7c0b NEO4J_TARBALL=neo4j-community-3.5.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:56:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.20-unix.tar.gz
# Thu, 30 Jul 2020 23:56:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.20-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:56:02 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Thu, 30 Jul 2020 23:56:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.20-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:56:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:56:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:56:16 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:56:16 GMT
COPY file:147c5d83a0e8f980042daf6c2540b40e96c165ebd51786a8d7697f8c1cd0cbc1 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:56:17 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:56:17 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:56:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a783655590e6fb36b581c0a5f4641bcc104fda44aec975db7fc08f978b1f42`  
		Last Modified: Fri, 31 Jul 2020 00:11:12 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82fd6a9c8cc2e21c86147f9e559c3174c4fb6591c621fc5e2835077b8fb5940`  
		Last Modified: Fri, 31 Jul 2020 00:11:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d54658de1f2cb1747971d94abe50f8084d706300f838e1a8997810df572b0e`  
		Last Modified: Fri, 31 Jul 2020 00:11:21 GMT  
		Size: 137.0 MB (136999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586fb7aa3de923314b98937fe435ef396e68a34c2a61042353a3a5863d602f8`  
		Last Modified: Fri, 31 Jul 2020 00:11:11 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.11`

```console
$ docker pull neo4j@sha256:fb830042d6a40fa6bbf864557f7b3396380a2c124e1f377e26b6f23cdc9ae7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.11` - linux; amd64

```console
$ docker pull neo4j@sha256:960593456aa416baf619e9495591324cf60fb14e9d1887f1724d3f8a0c446279
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228157749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f645ef082890b5ece571d700db52950d2786eb174fdff2e56adfc451bc5d7d`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:03:34 GMT
ENV NEO4J_SHA256=4dd4f2b6c32e216b42ab8d2235f10c4d992d567d36927df93d2d9fb1763e6376 NEO4J_TARBALL=neo4j-community-3.5.11-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:03:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.11-unix.tar.gz
# Fri, 31 Jul 2020 00:03:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.11-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:03:35 GMT
COPY multi:7cf12d6a82ce8caa397305af40147113f0c2e3f75bed74dbe4e434adf3288487 in /tmp/ 
# Fri, 31 Jul 2020 00:03:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:03:52 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:03:52 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:03:52 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:03:52 GMT
COPY file:8d85ed1b091a881aa7d34786c77b3933cd5f54de55a2d3f2248786eef97d873d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:03:52 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:03:53 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:03:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd67af07fbe12473814c49ce46352285132d70a1d3468decfd807a2d56c591c`  
		Last Modified: Fri, 31 Jul 2020 00:15:58 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d1c49791c4785ae0ba3b544b7470c8f1cdd8f97e753ae36064b9146a30da8b`  
		Last Modified: Fri, 31 Jul 2020 00:15:58 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f55620c46e34db928d5215170dd9678c76202f723195973023c70ce528a390`  
		Last Modified: Fri, 31 Jul 2020 00:16:23 GMT  
		Size: 157.2 MB (157193373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f47b67a28c7a8192e9c3b6e310db8d42f9cf31f6b7b57d6e03312268dba68`  
		Last Modified: Fri, 31 Jul 2020 00:15:58 GMT  
		Size: 5.3 KB (5251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.11-enterprise`

```console
$ docker pull neo4j@sha256:03a23b91cdd9e83bb3ce4b6fba1484bf4cdbf0df41b2954d03c3f15ef49a35f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.11-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:a2a63d48edf657428dd6783458602faed268755b5a5720fbe693ebeec0b4fb2f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263226421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853b54f928280e71a969645bf8fbb809f29b88848bc4bd2b42e8c3320a421a6c`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:03:59 GMT
ENV NEO4J_SHA256=e706a6a008bebc5fa06d97f671dc6099d1d1871020373c053a28f695964f88b2 NEO4J_TARBALL=neo4j-enterprise-3.5.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:03:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.11-unix.tar.gz
# Fri, 31 Jul 2020 00:04:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.11-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:04:00 GMT
COPY multi:7cf12d6a82ce8caa397305af40147113f0c2e3f75bed74dbe4e434adf3288487 in /tmp/ 
# Fri, 31 Jul 2020 00:04:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.11-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:04:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:04:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:04:19 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:04:19 GMT
COPY file:8d85ed1b091a881aa7d34786c77b3933cd5f54de55a2d3f2248786eef97d873d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:04:19 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:04:19 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:04:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6fc19d987ea3eba4a8ca262aef0f9697a1e2d9e855858291cf14fed6ae4f54`  
		Last Modified: Fri, 31 Jul 2020 00:16:26 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fe3cde65955504522285292c597d045576bd0d057b6c6d6b51112c25c8ce3f`  
		Last Modified: Fri, 31 Jul 2020 00:16:26 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caec013c75affd2d8f72b25364a1b7cdf907e7fe02bc9d78462ac8fe74054f07`  
		Last Modified: Fri, 31 Jul 2020 00:16:39 GMT  
		Size: 192.3 MB (192262046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07c425b97c64835201df73df13af7190307da6dbe290528f382fb4c20e4e665`  
		Last Modified: Fri, 31 Jul 2020 00:16:27 GMT  
		Size: 5.3 KB (5251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.12`

```console
$ docker pull neo4j@sha256:bfb18de39d43d5655cb8f6997497854fc816c3f49948aa160ea951e0ffe971c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.12` - linux; amd64

```console
$ docker pull neo4j@sha256:84eafc5e9fb23a9a581b2cd6237820ed86539bf5d01ff8b4de38fa04f05b489b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228353049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be2ab3d060d467dfd0e22b9b2a43c0654095e91bf72b5a98ab4b678795aa4b2`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:02:48 GMT
ENV NEO4J_SHA256=3b82b72a211d1b628b64f18f4af9f10b12ed6e2fd0ad94910e11b7fef5d0d86c NEO4J_TARBALL=neo4j-community-3.5.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:02:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.12-unix.tar.gz
# Fri, 31 Jul 2020 00:02:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.12-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:02:49 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:03:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:03:02 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:03:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:03:03 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:03:03 GMT
COPY file:8d85ed1b091a881aa7d34786c77b3933cd5f54de55a2d3f2248786eef97d873d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:03:03 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:03:03 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:03:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e15ec382f86e7038b5158c728c5d814c62ba4de180dad8fd68b0d0a7806e295`  
		Last Modified: Fri, 31 Jul 2020 00:15:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e8e81fa595c47c8427ae7f7073a1f57bb5db9a3fa2a75bf26eaf4cc217f7f`  
		Last Modified: Fri, 31 Jul 2020 00:15:14 GMT  
		Size: 303.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b7387a54486a4a4a63ba7668769eb10e91943f04ca95aa9ba27ed2a27d218`  
		Last Modified: Fri, 31 Jul 2020 00:15:27 GMT  
		Size: 157.4 MB (157388676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ddf7dd3b2dbb31fa09ff824cd755631f39109e3896da563e86e98886c3d7f1`  
		Last Modified: Fri, 31 Jul 2020 00:15:14 GMT  
		Size: 5.3 KB (5251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.12-enterprise`

```console
$ docker pull neo4j@sha256:081be6bd0315fe9eb6b7beb2536848ec6a694438389ffc77b904ff678585f635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.12-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:48ca5414204dec28fc35d14fabde5699cbb9d8eb1e5645d19cc7dfc90f097522
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263470311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917bb2d84bce2a251405eb679156512a1d97979d03089244232f7681dd595c69`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:03:09 GMT
ENV NEO4J_SHA256=bf23ff236aa5e4b15a840441d7e75d14ff3eb04de8e67edd291c23762be790cd NEO4J_TARBALL=neo4j-enterprise-3.5.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:03:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.12-unix.tar.gz
# Fri, 31 Jul 2020 00:03:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.12-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:03:10 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:03:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:03:29 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:03:29 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:03:29 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:03:29 GMT
COPY file:8d85ed1b091a881aa7d34786c77b3933cd5f54de55a2d3f2248786eef97d873d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:03:30 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:03:30 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:03:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218038c9b8b3aa22f1560c858caf7ecea40ae67bf7e196d1d328d43037f9d877`  
		Last Modified: Fri, 31 Jul 2020 00:15:31 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f505bd88a1d5b34fcbcb06f0da5a6f7514891347592e6e86f5478e906572ea`  
		Last Modified: Fri, 31 Jul 2020 00:15:31 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4340f5db5c82e35f4543650ae576b8e4527ec7ef3fdc2a6d0b7e831fb0f821ec`  
		Last Modified: Fri, 31 Jul 2020 00:15:53 GMT  
		Size: 192.5 MB (192505937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dba3d92b734bc806e781e6463062c960f4115b5e039158fdab1c391869967d`  
		Last Modified: Fri, 31 Jul 2020 00:15:31 GMT  
		Size: 5.2 KB (5248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.13`

```console
$ docker pull neo4j@sha256:9a9b92e3289028992b2a567441f09f483570f6c3b914aabc9db20cb6a90fec67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.13` - linux; amd64

```console
$ docker pull neo4j@sha256:bbb51361d66ed566c8f4fcba62fa024949dff36f1a1718478672d2418845f89d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230569576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a60bb0f32d4f8786dae73d1cd0467df55891e746719c6589c4392cd3ffdf0cf`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:01:56 GMT
ENV NEO4J_SHA256=2fdb29816bc72894b10f082b5d542fdaa0cf5d9cfdb899d9aac1e34bc2006250 NEO4J_TARBALL=neo4j-community-3.5.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:01:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.13-unix.tar.gz
# Fri, 31 Jul 2020 00:01:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.13-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:01:58 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:02:14 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:02:14 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:02:15 GMT
COPY file:af001fe5ddb05cac858c69f075bc3cd9077701dfa2891fe6c5a518755a596997 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:02:15 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:02:15 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:02:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a729ea25504408862633c4c19699d8f28d8eb359ce7fbb3edab966cbd16ee22`  
		Last Modified: Fri, 31 Jul 2020 00:14:41 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d471d9393ae55ad0d4824070eadcfc9b6cc1f689bc821b8b45863a75e0087dd`  
		Last Modified: Fri, 31 Jul 2020 00:14:41 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e34cded2e5c447244a15bcc9cc94134dcd56112234a2d10e14605b93e4b473e`  
		Last Modified: Fri, 31 Jul 2020 00:14:53 GMT  
		Size: 159.6 MB (159605203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536f42e7bece131ce773810f2b4659edca2bf4dbf835e6fa02b75b805f78557`  
		Last Modified: Fri, 31 Jul 2020 00:14:42 GMT  
		Size: 5.3 KB (5252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.13-enterprise`

```console
$ docker pull neo4j@sha256:42c59ee83201fbf90e2b39c99bfaa1e77d074ff15769e4e7d9ef26e18d7d45bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.13-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:01372e2974be37be7b123282627f85c2c70717059d437f03e21f8d4bd6de025b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265696970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4aee40e20273ea975eb4ed8d1118a072a6683478450be5371b729b233d2841`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:02:22 GMT
ENV NEO4J_SHA256=e1f74ed3923dc65498f4bf8b17a41d4e05e505e093c23e65ab3e6c47d1ca61af NEO4J_TARBALL=neo4j-enterprise-3.5.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:02:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.13-unix.tar.gz
# Fri, 31 Jul 2020 00:02:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.13-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:02:23 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:02:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:02:42 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:02:42 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:02:43 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:02:43 GMT
COPY file:af001fe5ddb05cac858c69f075bc3cd9077701dfa2891fe6c5a518755a596997 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:02:43 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:02:43 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:02:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbbf8ad3615540b2bdb8103913bc3889d68d20349836ca978a32dc4bdcc3f7d`  
		Last Modified: Fri, 31 Jul 2020 00:14:56 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9786b8005d60658bb26618a1ae4d2fe128cc812aa29b94535d54ceeeb9056ef`  
		Last Modified: Fri, 31 Jul 2020 00:14:57 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1498985fcb5bb875d353e0b3866567b480fdc124b5e36e65206c86289e92f2e5`  
		Last Modified: Fri, 31 Jul 2020 00:15:10 GMT  
		Size: 194.7 MB (194732602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b7dc0904c0722832a2c839eb311dc6449f7d38c9ec4b0604cf9d0d2d5a8b9d`  
		Last Modified: Fri, 31 Jul 2020 00:14:57 GMT  
		Size: 5.3 KB (5252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.14`

```console
$ docker pull neo4j@sha256:7760bdd1f9555b9fd5c07bdf0730ed08b262d02b4699242f1a61f8539ebb4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.14` - linux; amd64

```console
$ docker pull neo4j@sha256:e634ce7e74fee844d659c84dc7107c414adc1906c3acbc5baee6e16a4385011e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229484844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751dc7a350b3d1a87f459d1fd7cd8c73bd631c1d9b4aa0da00b48945ea499913`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:01:02 GMT
ENV NEO4J_SHA256=fb435b11494cde475f748f057a192bcbd8580c7445b380afe9ff52311f334bfe NEO4J_TARBALL=neo4j-community-3.5.14-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:01:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.14-unix.tar.gz
# Fri, 31 Jul 2020 00:01:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.14-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:01:03 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:01:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.14-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:01:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:01:21 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:01:21 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:01:21 GMT
COPY file:7ffb493993f443c8153ccfe7de8510ab04c58686ca8ed69aed987a3e80542d26 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:01:22 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:01:22 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:01:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d8c37d895f05fcbd5e46c840bdf31422e7cdc6746966a29f0f704a90ac6f04`  
		Last Modified: Fri, 31 Jul 2020 00:14:09 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48440b2a925519c1f8cf57c5188ac352f8b949e8ac0605c1b4d4edf8b642fa37`  
		Last Modified: Fri, 31 Jul 2020 00:14:09 GMT  
		Size: 302.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7103d70310bcddd75a9266661dc2891ecd1180f6ab1deda1297a51c124dfcad9`  
		Last Modified: Fri, 31 Jul 2020 00:14:19 GMT  
		Size: 158.5 MB (158520311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12881be26bdd76c6da9f725859b7f3893b96bc571aea39fc924dafaa549db389`  
		Last Modified: Fri, 31 Jul 2020 00:14:09 GMT  
		Size: 5.4 KB (5411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.14-enterprise`

```console
$ docker pull neo4j@sha256:26d349b7461332fd76bc1c730334509a941505fca82b335e12e5c6a65b6950d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.14-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:052ccd03a0b4b3dfca413b81e02dbf86c641a31dad37f40140aa76ec999e7890
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264603496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc27322bd81a1d4a128d66895353a82294cd8b9df867ce85bc0b8dc615507f`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:01:28 GMT
ENV NEO4J_SHA256=8d02047f3196c23849f7b6dda605b98098dbdc694747f1708e119715af3d3e06 NEO4J_TARBALL=neo4j-enterprise-3.5.14-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:01:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.14-unix.tar.gz
# Fri, 31 Jul 2020 00:01:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.14-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:01:29 GMT
COPY multi:70b59ed932367b04ea9c69354feb959e63e40f0dd9086b2097eaeba453964337 in /tmp/ 
# Fri, 31 Jul 2020 00:01:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.14-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:01:50 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:01:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:01:50 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:01:50 GMT
COPY file:7ffb493993f443c8153ccfe7de8510ab04c58686ca8ed69aed987a3e80542d26 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:01:51 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:01:51 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:01:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ca269d385e5aab579839974c1c5d186cc748a2a08fffb4b17b497aff6df1b8`  
		Last Modified: Fri, 31 Jul 2020 00:14:24 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaae3f5f91be0ad552b5f00db1c215d8f0785e317d887fa7585fc8f082f024b`  
		Last Modified: Fri, 31 Jul 2020 00:14:23 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0472216e98f5de9536488f1a484ea2b0ddb82f447dccd2af9cb16a29d4c5b399`  
		Last Modified: Fri, 31 Jul 2020 00:14:36 GMT  
		Size: 193.6 MB (193638965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52efb8859b5e2e471fdf61d4bde71d566d9d753d1d39cf16c5c031e368f9ae42`  
		Last Modified: Fri, 31 Jul 2020 00:14:23 GMT  
		Size: 5.4 KB (5411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.15`

```console
$ docker pull neo4j@sha256:4ba3d3f24abdeb56aed48b1c297209ae3a05db5dde761bfb00924c7448f1c3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.15` - linux; amd64

```console
$ docker pull neo4j@sha256:c1c4216fed1a273eab34aa2e42fb26740fe21ec3d60d74bf4c81c1bf36732429
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206750577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677fe98df0e06f99871783a63b4f6fa45100f8561dd99a97f37b903b31edb90d`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:00:11 GMT
ENV NEO4J_SHA256=32ed30e81aed0fc32d7ca8245b4a25e7aa1c08b89770ea33da1f4b427f1f7664 NEO4J_TARBALL=neo4j-community-3.5.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:00:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.15-unix.tar.gz
# Fri, 31 Jul 2020 00:00:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.15-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:00:13 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 31 Jul 2020 00:00:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.15-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:00:29 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:00:30 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:00:30 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:00:30 GMT
COPY file:2302715b081c832649219f56c02e31f4562056b8ba8cd7c7dd5e1cf549d9e537 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:00:30 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:00:30 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:00:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b69a5773f131dc229ff74c5621b03b80b33b2841e2dcd0c4300739bebdd74d`  
		Last Modified: Fri, 31 Jul 2020 00:13:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f8ea6bc609aa54c3da74acb75d0924eb502e609a65a50a46f2acda47d6cf03`  
		Last Modified: Fri, 31 Jul 2020 00:13:39 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d37960d8d36dbbcf49e9ec971f8286ab24cce8aeda5f84fceafb899ffc270f0`  
		Last Modified: Fri, 31 Jul 2020 00:13:50 GMT  
		Size: 135.8 MB (135785428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a54c4d233fbe5977ae2f5f3398a8076debe89de727c18b26adbe80472af8b2`  
		Last Modified: Fri, 31 Jul 2020 00:13:39 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.15-enterprise`

```console
$ docker pull neo4j@sha256:3ddcfa9839d6eaf41bd76495e41a9a20d79a38f12e45940c5434b8c7de7138a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d1953815b301c51b3439f2de10e2351f0a2fd375ac129bd5bd89ae5c5a37a789
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241878884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7570ce5a5c460d6aa628381ec0959067e7d93b72a63a625e544db1500d81e8db`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:00:37 GMT
ENV NEO4J_SHA256=0d179b9e7f15c9d63a4b488976117012320b7ba6c8d9ccdca16342d392ea820a NEO4J_TARBALL=neo4j-enterprise-3.5.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:00:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.15-unix.tar.gz
# Fri, 31 Jul 2020 00:00:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.15-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:00:38 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 31 Jul 2020 00:00:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.15-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:00:56 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:00:56 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:00:57 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:00:57 GMT
COPY file:2302715b081c832649219f56c02e31f4562056b8ba8cd7c7dd5e1cf549d9e537 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:00:57 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:00:57 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:00:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db45c17ec616937f3f2fa4b65a0d40556d745ba97bf9afec5f64afd154edc75`  
		Last Modified: Fri, 31 Jul 2020 00:13:53 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bd5be4f1a63957c63d53e61b13111d32f27e357835344a18a57b26bec8d810`  
		Last Modified: Fri, 31 Jul 2020 00:13:53 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884dcd4ff14364052fb21b4088e3a8f90731ff213fe9db7ea2ed1cb8dcb1e688`  
		Last Modified: Fri, 31 Jul 2020 00:14:04 GMT  
		Size: 170.9 MB (170913730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f782c0df818bb5a7fa5cf516f64ce481b949b2782aaea350292117d5863b82b9`  
		Last Modified: Fri, 31 Jul 2020 00:13:53 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.16`

```console
$ docker pull neo4j@sha256:8158379a434bc3e6ff67b6a4905febc577fa9e9c7c8b426e70ba4a9f51288f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.16` - linux; amd64

```console
$ docker pull neo4j@sha256:8e9721b30cd87d3b96b8088da34eea8034503baf8d298a34917a012dc9b258f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206756543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f635433efdb59ab5db5c352a632c1a10f99cf3f7d0658d459c18299c91582ae`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:59:17 GMT
ENV NEO4J_SHA256=3eded9065de1ddd39d519b05845da2f572b5ddb4e6440b93555927f329eaf222 NEO4J_TARBALL=neo4j-community-3.5.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:59:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.16-unix.tar.gz
# Thu, 30 Jul 2020 23:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.16-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:59:18 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Thu, 30 Jul 2020 23:59:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.16-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:59:34 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:59:34 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:59:35 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:59:35 GMT
COPY file:2302715b081c832649219f56c02e31f4562056b8ba8cd7c7dd5e1cf549d9e537 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:59:35 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:59:35 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37455cf050ed1b3667944ef23f903c344210b8cfa55c4bc0efb8059db236daac`  
		Last Modified: Fri, 31 Jul 2020 00:13:11 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865f86544eedba44e329ffd0318f2cccb03e9f44adaf8fff6f893fc9ebdeebb9`  
		Last Modified: Fri, 31 Jul 2020 00:13:11 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca10f85cc25b1d4a68c3871eb324896706ece0f195075b426b4d9e3aea0fff`  
		Last Modified: Fri, 31 Jul 2020 00:13:21 GMT  
		Size: 135.8 MB (135791396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13183cde323a514e55f6f5dfc98745fc42aa54a2352fe250dd2ec707328b38ea`  
		Last Modified: Fri, 31 Jul 2020 00:13:11 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.16-enterprise`

```console
$ docker pull neo4j@sha256:18f7ba6764ebd8c5b987ca9bf3ffdff71ed4307df3bc891025a9a1ba8be3aa47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:4ae45b0e33168fcb9df96071e05324c6196d015cb55dd4d15dc513cabed86e52
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241887630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df040b25e6b794377dbe6cb548e7f6fb178ed0828bc14c8a878c2d017fc01cd5`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:59:43 GMT
ENV NEO4J_SHA256=38dfbaa88b2b17eeb8ec7cf4362327b08f04dd2733374541ba6f233fba6560b2 NEO4J_TARBALL=neo4j-enterprise-3.5.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:59:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.16-unix.tar.gz
# Thu, 30 Jul 2020 23:59:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.16-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:59:44 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Fri, 31 Jul 2020 00:00:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.16-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Fri, 31 Jul 2020 00:00:02 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:00:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:00:03 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:00:03 GMT
COPY file:2302715b081c832649219f56c02e31f4562056b8ba8cd7c7dd5e1cf549d9e537 in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:00:03 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:00:03 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:00:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c4d9d0b735d11256fc54c2dac176d1cdeb68080a0b855368d02ce020092ca2`  
		Last Modified: Fri, 31 Jul 2020 00:13:24 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8b7570790cf3c259525bcba9e23b7bf043e1348d54cb42712061fca786ece4`  
		Last Modified: Fri, 31 Jul 2020 00:13:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f0d115bb93aa53589c299559016492df155c7a286b390812684b074d5bae3f`  
		Last Modified: Fri, 31 Jul 2020 00:13:36 GMT  
		Size: 170.9 MB (170922476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5fbd498611bc8b0b3913bdd7e619ba9b709d8f436169d6f2ff20da363b5a41`  
		Last Modified: Fri, 31 Jul 2020 00:13:24 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.17`

```console
$ docker pull neo4j@sha256:fb3908624b4a2843228f0159f3410a88668b2cb86fbadd39bd0414d5e99dc6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.17` - linux; amd64

```console
$ docker pull neo4j@sha256:a7e3b0722ec4862144256b55785517c7bd4df39666ff6cd1f286361ed5c5489c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206804624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62ed43d08cab4bd8a1b3e6c2f771cf7cb9d77a0a425a702f592fa1e971355cf`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:58:26 GMT
ENV NEO4J_SHA256=1c8b6ac0ffd346f0707fe1af713ef74f1c6ce1ea6feb5e9a0bd170e7a8a34a10 NEO4J_TARBALL=neo4j-community-3.5.17-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:58:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
# Thu, 30 Jul 2020 23:58:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:58:28 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Thu, 30 Jul 2020 23:58:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.17-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:58:44 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:58:45 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:58:45 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:58:45 GMT
COPY file:cd969a3e3d21f58e9a9a346d321ec15de0b681e0976dc4b74a6a00cb6cd0f32c in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:58:45 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:58:45 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:58:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4fc7653f1e43db08a537d4bacbbe705d85801dce02bed5a331c8bbe12c4f96`  
		Last Modified: Fri, 31 Jul 2020 00:12:40 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6caa1a08ca6e1462cbf39fd20ff7a693d96ad9bebbfbf1b36c291f410faaada2`  
		Last Modified: Fri, 31 Jul 2020 00:12:40 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107fe5f015e6fdf3e262a231b6d87e108beb940a3652c054ddca8188f042f0d`  
		Last Modified: Fri, 31 Jul 2020 00:12:49 GMT  
		Size: 135.8 MB (135839477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957157ccaac98a0fcccd2d2c30935788215ba87045fdb45c9bc99f1e1171f876`  
		Last Modified: Fri, 31 Jul 2020 00:12:40 GMT  
		Size: 5.9 KB (5881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.17-enterprise`

```console
$ docker pull neo4j@sha256:a3e8f296a518fb88b6721f3c3bb2b2e8170be91e6881d823e03cfd3d571a8f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.17-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c71973ade0fd5e1a3e59a4f47940377bae8094116d84009b897127c93fcb73ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241936156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8f570440e2ce665f6bc8acce6846e6668e357cfa4ff86802daa2ebf6cd3d6b`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:58:51 GMT
ENV NEO4J_SHA256=1f8c60e01e8bcdb5c6921341bd4a783c08a748cabb3348d4e4d2f104544232ca NEO4J_TARBALL=neo4j-enterprise-3.5.17-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:58:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
# Thu, 30 Jul 2020 23:58:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:58:53 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Thu, 30 Jul 2020 23:59:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.17-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:59:11 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:59:11 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:59:11 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:59:11 GMT
COPY file:cd969a3e3d21f58e9a9a346d321ec15de0b681e0976dc4b74a6a00cb6cd0f32c in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:59:11 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:59:12 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:59:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d425403ecd62c108918fb8444b0f5aba34ee18bc4938a07a2903c6893f6f55`  
		Last Modified: Fri, 31 Jul 2020 00:12:53 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76656081c45f29570cf0824175c1526a0286012bc58ce81eafa2cc0a62f18500`  
		Last Modified: Fri, 31 Jul 2020 00:12:53 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcabdc4d70ad9246fe636fb08fd942936c45b4dc615e8b04dcc0bfdd93af7d43`  
		Last Modified: Fri, 31 Jul 2020 00:13:07 GMT  
		Size: 171.0 MB (170971005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905c6296a18b50b4f22afeaaa139d531dad431618f8e19de39f226c0da468dbd`  
		Last Modified: Fri, 31 Jul 2020 00:12:53 GMT  
		Size: 5.9 KB (5881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.18`

```console
$ docker pull neo4j@sha256:282732a14cb4731564f0ea124eeafda24bb96bedbf96d06d0878a6adf669cd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.18` - linux; amd64

```console
$ docker pull neo4j@sha256:473b660c533ea55f24848321af6c61afd4f5a6899ac0495ae9a906559eb55614
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206828425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49308af01e15842e4a4a535c794b447ac1c0216368a8f01ec95bb0f9fe5619e`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:57:39 GMT
ENV NEO4J_SHA256=ed6c2c52faf048919cea6da8f214071b57e3cdcfae4527957d25948a35c6c75a NEO4J_TARBALL=neo4j-community-3.5.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:57:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.18-unix.tar.gz
# Thu, 30 Jul 2020 23:57:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.18-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:57:40 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Thu, 30 Jul 2020 23:57:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.18-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:57:56 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:57:56 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:57:57 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:57:57 GMT
COPY file:147c5d83a0e8f980042daf6c2540b40e96c165ebd51786a8d7697f8c1cd0cbc1 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:57:57 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:57:57 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:57:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c490d83b00c7696a846167b51ac8577d993697bae6e4ef7527d1907abe35b0`  
		Last Modified: Fri, 31 Jul 2020 00:12:10 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690c371cef580db74a375a727b92d3a12a6e82cb5a8068bb204b236aaafd6a29`  
		Last Modified: Fri, 31 Jul 2020 00:12:10 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199732bd381f01fac68746cf5aaeb22189b326425145b548af796657da6c9388`  
		Last Modified: Fri, 31 Jul 2020 00:12:20 GMT  
		Size: 135.9 MB (135863263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7576758954a39222ddd3fc44a849c36233d063a40354bf61ce5ea24c2e8fa75`  
		Last Modified: Fri, 31 Jul 2020 00:12:10 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.18-enterprise`

```console
$ docker pull neo4j@sha256:68193f3a7ef1e3baa37126f8c0ed0ef1c7d7a1412dd8b7a196a23ff349743312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.18-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:f77dcaf2a831c5efa12cd3fb3de3baa7241f9b2fc96b3cfc3afe8580b0dd6a70
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (241959125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fef8a9389f19e8e172dbeb8c9b832a06823c532e7a61c43f8457a95d0082e38`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:58:04 GMT
ENV NEO4J_SHA256=ee31452f857480b4843ebcf05ee96f2431ecdabe442b90bc2c75a5cc9f1dd46e NEO4J_TARBALL=neo4j-enterprise-3.5.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:58:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.18-unix.tar.gz
# Thu, 30 Jul 2020 23:58:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.18-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:58:06 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Thu, 30 Jul 2020 23:58:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.18-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:58:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:58:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:58:21 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:58:21 GMT
COPY file:147c5d83a0e8f980042daf6c2540b40e96c165ebd51786a8d7697f8c1cd0cbc1 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:58:22 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:58:22 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:58:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce97c353f3d4b2f734e56de0c7f8a2244f3128552ef84bffe085a3a01fa73206`  
		Last Modified: Fri, 31 Jul 2020 00:12:24 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d566b3dd0cfed75083420d5ee809a8481d353ab83351581aafbbd31d1ac4f7e`  
		Last Modified: Fri, 31 Jul 2020 00:12:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4189b30f56912ada27b59bef8c9a31e2342a492688b75657591cdef08dd9dffa`  
		Last Modified: Fri, 31 Jul 2020 00:12:36 GMT  
		Size: 171.0 MB (170993968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1846bedf9aabe35dea8d312f3e553e54b6b4b7396c53f1e7554ae38d8b6d59`  
		Last Modified: Fri, 31 Jul 2020 00:12:24 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.19`

```console
$ docker pull neo4j@sha256:de25e2e51f37de4668887338f58d71e2822bbdfb23843f5345a7d05b7d8f2e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.19` - linux; amd64

```console
$ docker pull neo4j@sha256:67781d453888486c652bf778cd6eda969244448d067e4ac88d8fc84d654446e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206848580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d49548f5174e38334a7493118686540162fb5b1acdb1e85abb1f3a086175003`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:56:48 GMT
ENV NEO4J_SHA256=c0b514af785fb5649963706d98864cc690397e14b3ff3942ec8dabf02c2f768a NEO4J_TARBALL=neo4j-community-3.5.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:56:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.19-unix.tar.gz
# Thu, 30 Jul 2020 23:56:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.19-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:56:49 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Thu, 30 Jul 2020 23:57:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.19-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:57:05 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:57:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:57:06 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:57:06 GMT
COPY file:147c5d83a0e8f980042daf6c2540b40e96c165ebd51786a8d7697f8c1cd0cbc1 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:57:06 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:57:07 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:57:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043fa19c4cbc8344955453c2be804560ad90ebc1e9f1005f8e04516c287b2e3`  
		Last Modified: Fri, 31 Jul 2020 00:11:41 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908be3ba753b2760cc1f32d932483bd741ea9a8ea21d28672daed100ddff6077`  
		Last Modified: Fri, 31 Jul 2020 00:11:41 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038645efad0d6b8cd616e79b3db3d9024d6459f1b7aecb3b4c229cefe71af375`  
		Last Modified: Fri, 31 Jul 2020 00:11:52 GMT  
		Size: 135.9 MB (135883425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dc9021f1f96841b930ad4a5a00287a9e0584d66de5d8cb6e62e0328d103ab9`  
		Last Modified: Fri, 31 Jul 2020 00:11:41 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.19-enterprise`

```console
$ docker pull neo4j@sha256:7799202db540b41143eec0224f67c8bde7a45fa72a21a128d04240562856e335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.19-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:53dd1d1db2c53202becd3f48c417f1c639cc73c3bc2788760533371f736ccc43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (241979047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bb31d42d113194ccc5efc06b839b2506a2ee421e48c8b516744bde2090e495`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:57:14 GMT
ENV NEO4J_SHA256=a470e9502985348ef9ea9a10b50eddb0df0d692505faadedbc53fe7804d339c9 NEO4J_TARBALL=neo4j-enterprise-3.5.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:57:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.19-unix.tar.gz
# Thu, 30 Jul 2020 23:57:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.19-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:57:16 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Thu, 30 Jul 2020 23:57:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.19-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:57:31 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:57:31 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:57:32 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:57:32 GMT
COPY file:147c5d83a0e8f980042daf6c2540b40e96c165ebd51786a8d7697f8c1cd0cbc1 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:57:32 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:57:32 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:57:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08980fefd32085545b2a98a1992f3d2288b5bee022426b6b1c1dd8b9e8bfc7a9`  
		Last Modified: Fri, 31 Jul 2020 00:11:55 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269b2ca65cb8cfcf60f3e89bfa4237aaea8014158ca60299d11b1e6cee7349c7`  
		Last Modified: Fri, 31 Jul 2020 00:11:55 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6b9dc841e13015abcda50105f042032be362c569678b9d9baf4e35ac9734d9`  
		Last Modified: Fri, 31 Jul 2020 00:12:07 GMT  
		Size: 171.0 MB (171013890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f79431ffbed6fbec967847379dc02e7cf99ab0894e0bdfdcf35d2183063ce1`  
		Last Modified: Fri, 31 Jul 2020 00:11:55 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.20`

```console
$ docker pull neo4j@sha256:677cb9e83988bb0947ceedf9183ade957cd550adaab187c23f208b2c6d343e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.20` - linux; amd64

```console
$ docker pull neo4j@sha256:37e8c844c117e0bf413293b6c2ba843ccf3207d3dbcb10cb8d2de474082685a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207964606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84698499aef66b7a5bdd7beb69b0a0171efb9f2f8c20cfa5a80fd3f756527be`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:56:01 GMT
ENV NEO4J_SHA256=01406d4e6a9e89340637aac779adb189db9af66e9c615804ad1ccc17346c7c0b NEO4J_TARBALL=neo4j-community-3.5.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:56:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.20-unix.tar.gz
# Thu, 30 Jul 2020 23:56:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.20-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:56:02 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Thu, 30 Jul 2020 23:56:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-3.5.20-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:56:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:56:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:56:16 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:56:16 GMT
COPY file:147c5d83a0e8f980042daf6c2540b40e96c165ebd51786a8d7697f8c1cd0cbc1 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:56:17 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:56:17 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:56:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a783655590e6fb36b581c0a5f4641bcc104fda44aec975db7fc08f978b1f42`  
		Last Modified: Fri, 31 Jul 2020 00:11:12 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82fd6a9c8cc2e21c86147f9e559c3174c4fb6591c621fc5e2835077b8fb5940`  
		Last Modified: Fri, 31 Jul 2020 00:11:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d54658de1f2cb1747971d94abe50f8084d706300f838e1a8997810df572b0e`  
		Last Modified: Fri, 31 Jul 2020 00:11:21 GMT  
		Size: 137.0 MB (136999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586fb7aa3de923314b98937fe435ef396e68a34c2a61042353a3a5863d602f8`  
		Last Modified: Fri, 31 Jul 2020 00:11:11 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.20-enterprise`

```console
$ docker pull neo4j@sha256:94029b29b5ee9a45b3cb4edff3e3b721d6d7e4f50ce875de7d36eac9ff092f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.20-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:de9d498fa3566e7644e9e80eb937f7a652c837f32a79c0e21c95b32428735df0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243092953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e4a818d3cc1d1a88e6a5ca11f0ad4f310e93d17b9f08d104c4ceee0713a6c8`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:56:23 GMT
ENV NEO4J_SHA256=29d7a205c27f786413abd61c462ddd67ab888042275a0f753a4912c49b501b5e NEO4J_TARBALL=neo4j-enterprise-3.5.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:56:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.20-unix.tar.gz
# Thu, 30 Jul 2020 23:56:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.20-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:56:24 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Thu, 30 Jul 2020 23:56:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.20-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:56:42 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:56:42 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:56:43 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:56:43 GMT
COPY file:147c5d83a0e8f980042daf6c2540b40e96c165ebd51786a8d7697f8c1cd0cbc1 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:56:43 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:56:43 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:56:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232f69f3145c170f151f9cc44dcd367008be0d140ea1be8c30d6555a04fcdf67`  
		Last Modified: Fri, 31 Jul 2020 00:11:25 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6496262f4379818071e7e0c0dbba2233a2d6f8b2e77d7b796cb4a42f1bcccd9`  
		Last Modified: Fri, 31 Jul 2020 00:11:25 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10994a8b879e82d692f14d393620db6d0c293a2ecba3d813048bc34ccf28460b`  
		Last Modified: Fri, 31 Jul 2020 00:11:37 GMT  
		Size: 172.1 MB (172127795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d76911747985921148e5096079586196406dd90e60bb0f24cf3f279f9ae2f3`  
		Last Modified: Fri, 31 Jul 2020 00:11:25 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.6`

```console
$ docker pull neo4j@sha256:6ab9800c30282406124d66ae24ffaf16c71d5043ab92bba195e29e2972997aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.6` - linux; amd64

```console
$ docker pull neo4j@sha256:8d105805fd92bfb20f309816b466ff28ef2ba1c4a375500ab569378a2f0f4ed0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240940293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae96d84f1d5606235003091488b036c1362cbed5a52f4867c3a929d882416496`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:06:02 GMT
ENV NEO4J_SHA256=f536224565ce27b95947c91a37d52b9ba9e80247d8d3262075b24b8d47f8532a NEO4J_TARBALL=neo4j-community-3.5.6-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:06:02 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.6-unix.tar.gz
# Fri, 31 Jul 2020 00:06:03 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.6-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:06:03 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:06:19 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.6-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 31 Jul 2020 00:06:19 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:06:19 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:06:19 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:06:20 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:06:20 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:06:20 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:06:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d50de975d4d97812fe67be8df9d2764f8cc0cb64c8930c3ae1698ed3a27bb`  
		Last Modified: Fri, 31 Jul 2020 00:18:10 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605ed37b87b18b3ffc6a312d4eea0442f25c91bf9dd5b513645260e7854b9381`  
		Last Modified: Fri, 31 Jul 2020 00:18:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a2fc7ecefffebdcaf787329ec9757da75e616a8bdb8423165dbe001c563cd5`  
		Last Modified: Fri, 31 Jul 2020 00:18:23 GMT  
		Size: 170.0 MB (169976959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1019946c46433027a2b1704615e4d5f5738e7ad65c156c609f8444f50b8383b`  
		Last Modified: Fri, 31 Jul 2020 00:18:10 GMT  
		Size: 4.4 KB (4386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.6-enterprise`

```console
$ docker pull neo4j@sha256:d21801535dcb39a171f7b7ffda472d01572eeccdc15161337f900b2f34b5bf52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.6-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:71c13e09e05db0aab66d0f389b68acf6d6e2491792613b606c5047acacee9c79
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276029304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25403230224e691a44ca545b514b92981d13a61c7bfedd2a60307a6ee59c8faf`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:06:24 GMT
ENV NEO4J_SHA256=0d738dd5bd04aaf15c672e27833480339de5bbe85a56cc932bd15aa27fb99509 NEO4J_TARBALL=neo4j-enterprise-3.5.6-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:06:24 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.6-unix.tar.gz
# Fri, 31 Jul 2020 00:06:25 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.6-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:06:26 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:06:43 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.6-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 31 Jul 2020 00:06:43 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:06:44 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:06:44 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:06:44 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:06:44 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:06:44 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:06:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e38138de80e89e2166bac9ec9b4c7e6709ee08c171fefc89290ce8fec8913c`  
		Last Modified: Fri, 31 Jul 2020 00:18:27 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba73f73a2b48b0bcd84af0854f9272f7db4fdd26b197639520507e7a4adfbc5`  
		Last Modified: Fri, 31 Jul 2020 00:18:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a77983408ab3bb818062ca295ba342aa981942c993f8b12fb1e8b791b8ff4e`  
		Last Modified: Fri, 31 Jul 2020 00:18:41 GMT  
		Size: 205.1 MB (205065974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72af6f644e4e670409e7e6aeaba0a6e3a3df89d4d6251eb8414779efcd654d8`  
		Last Modified: Fri, 31 Jul 2020 00:18:27 GMT  
		Size: 4.4 KB (4384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.7`

```console
$ docker pull neo4j@sha256:eece636fdf7624770991fdef30b3470437836bfdb97191854ecbd7406e5ce690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.7` - linux; amd64

```console
$ docker pull neo4j@sha256:a6fb1937e4194a991e6d8826703be22f3f79aec5463c8ac58b64207c3212fa67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241005050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6806d831b1786c7866c80cab953ffc1300b8f1b064ca35a1d194a64b0eb8f3c4`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:05:15 GMT
ENV NEO4J_SHA256=31c8f398df9342928502a7321f045eb8f2b96ec4ded26f9f057dc6f6fa10c60c NEO4J_TARBALL=neo4j-community-3.5.7-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:05:15 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.7-unix.tar.gz
# Fri, 31 Jul 2020 00:05:16 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.7-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:05:16 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:05:31 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.7-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 31 Jul 2020 00:05:32 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:05:32 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:05:32 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:05:32 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:05:32 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:05:33 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:05:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b09a471f9b3fca99fd446026ad4ce60e54f08251b9340db9e319a524d8c8739`  
		Last Modified: Fri, 31 Jul 2020 00:17:30 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649f6374017b24574e8af5965b45a28754a772948d231f0fa2cd33181aed867c`  
		Last Modified: Fri, 31 Jul 2020 00:17:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c699e2e2404b3ca52d789e7b61c64971f3bad12b6181d0b3d761e17088f59a5`  
		Last Modified: Fri, 31 Jul 2020 00:17:42 GMT  
		Size: 170.0 MB (170041713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627b4e576503d5ba32a9900e81d6fec1fab81ed79dbab7b20de9d6136f71e9ab`  
		Last Modified: Fri, 31 Jul 2020 00:17:30 GMT  
		Size: 4.4 KB (4386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.7-enterprise`

```console
$ docker pull neo4j@sha256:a6c73cf1ecf4e3443280377659e8c250087436cc23e91171b14274a9f7c43ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.7-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:62944381feb91af7bc257f42db065220f42e465a46ac816d391fe900f32ec09e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276127162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b9a899a7853c916f163aac503985a698fe2beb6e2dcc45d340fb5cf881ced5`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:05:37 GMT
ENV NEO4J_SHA256=f4585c82e43c52d06db3c4194a62766c20adea3566fcc9e9992e3f19d3311e14 NEO4J_TARBALL=neo4j-enterprise-3.5.7-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:05:37 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.7-unix.tar.gz
# Fri, 31 Jul 2020 00:05:38 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.7-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:05:38 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:05:55 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.7-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs
# Fri, 31 Jul 2020 00:05:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:05:55 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:05:56 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:05:56 GMT
COPY file:a6df7d0365e68d6518a68c4e06867141cbce4a327fb803991d77cb4c971aed5d in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:05:56 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:05:56 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:05:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434fe8a7536c8deec42cdc3a138c2054706301363e34d657e6b2082ff7e7f8d4`  
		Last Modified: Fri, 31 Jul 2020 00:17:49 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c36e62e753db1f00d4de4210c92469e8bbe5bc07c6cc930d254d203da7ed23`  
		Last Modified: Fri, 31 Jul 2020 00:17:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e5ccfaff2e051ab8ceab086a031fac392ba4520df24f22a67c1b7bccb0e412`  
		Last Modified: Fri, 31 Jul 2020 00:18:03 GMT  
		Size: 205.2 MB (205163832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2567ffd58c075fedbf01e4bde39cfaa0884efbbd5f69b2dce5c3de86f9990dfb`  
		Last Modified: Fri, 31 Jul 2020 00:17:49 GMT  
		Size: 4.4 KB (4386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.8`

```console
$ docker pull neo4j@sha256:106d2f452163ea333c809909d6bd60fe5d8a3e210997b00bd2ca79fcafbbcc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.8` - linux; amd64

```console
$ docker pull neo4j@sha256:907c5558eae52460348d840aec564c782a0204dd3a0deae0033edd8b9d8c2634
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227579496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8924b74a244cf386d656e7f7657b65ccc05259607bece5fc5bc41c92f508b9a1`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:04:25 GMT
ENV NEO4J_SHA256=ef714d0e7067d437649e52b6727d258c46a144db2ce567dc4d13b62ee916494e NEO4J_TARBALL=neo4j-community-3.5.8-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:04:25 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.8-unix.tar.gz
# Fri, 31 Jul 2020 00:04:26 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.8-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:04:26 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:04:42 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-community-3.5.8-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:04:42 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:04:42 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:04:42 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:04:43 GMT
COPY file:e07128b8290e38440521f56bbf78b61bbce8be21a97b8b31668594bebdd2bf2b in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:04:43 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:04:43 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:04:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5946734ffa79c0af5af108fe553abcd1688c79164ec9abfcff7c4cb9b4489f`  
		Last Modified: Fri, 31 Jul 2020 00:16:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ca9894498350298464c3081ca727dc799bfd88dcf10e603df29674cfa3545`  
		Last Modified: Fri, 31 Jul 2020 00:16:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24605cbad39689cf331629a9a91e3010187e6262253a65a16c3fbc9309447af6`  
		Last Modified: Fri, 31 Jul 2020 00:16:55 GMT  
		Size: 156.6 MB (156616194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be269d40338a09d8c0611dc7ed14bc3436f3f9291f64bcd8f327f29732d0e91`  
		Last Modified: Fri, 31 Jul 2020 00:16:44 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5.8-enterprise`

```console
$ docker pull neo4j@sha256:b990b8db2ca1d563c095f5363d98257f4f925fcf26e4d7556227303d829199c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5.8-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e9871ac4d8c16a76d13a88c04e5cd7be6e20987efaf69192bfd3b21f91b14688
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262713204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a333b3b9c611a94ca37d964016d173b424f02c029a03239ba604ffb1c373762a`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 31 Jul 2020 00:04:50 GMT
ENV NEO4J_SHA256=29b854cc540b608d86236102417b7d3d06a027e28eb3d9be8fbf7931f713bca3 NEO4J_TARBALL=neo4j-enterprise-3.5.8-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Fri, 31 Jul 2020 00:04:50 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.8-unix.tar.gz
# Fri, 31 Jul 2020 00:04:52 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.8-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 31 Jul 2020 00:04:52 GMT
COPY file:696befc481f5ad55a590fa577c3d4ba04c9237326d85b95b729538f95702e110 in /tmp/ 
# Fri, 31 Jul 2020 00:05:09 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.5.8-unix.tar.gz
RUN apt update     && apt install -y curl gosu     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Jul 2020 00:05:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 00:05:09 GMT
WORKDIR /var/lib/neo4j
# Fri, 31 Jul 2020 00:05:10 GMT
VOLUME [/data /logs]
# Fri, 31 Jul 2020 00:05:10 GMT
COPY file:e07128b8290e38440521f56bbf78b61bbce8be21a97b8b31668594bebdd2bf2b in /docker-entrypoint.sh 
# Fri, 31 Jul 2020 00:05:10 GMT
EXPOSE 7473 7474 7687
# Fri, 31 Jul 2020 00:05:10 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 31 Jul 2020 00:05:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded88f89cccb7492aee04d02b6cc0439d9ae7aa17282804a2d625ba4ffe0fc0d`  
		Last Modified: Fri, 31 Jul 2020 00:16:59 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98af959ca10461d0555923b66878a763daaa85bccbfad29995b0db34c3f2c744`  
		Last Modified: Fri, 31 Jul 2020 00:17:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e60268ddb6579966c38554b0c07cc0e6a0adcc019ac76b6d39c699b8a31979`  
		Last Modified: Fri, 31 Jul 2020 00:17:25 GMT  
		Size: 191.7 MB (191749909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb01f7f406c38588d6107268e9582278756203fbbcab997e7408a69cada56cd`  
		Last Modified: Fri, 31 Jul 2020 00:16:59 GMT  
		Size: 4.3 KB (4348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:3.5-enterprise`

```console
$ docker pull neo4j@sha256:94029b29b5ee9a45b3cb4edff3e3b721d6d7e4f50ce875de7d36eac9ff092f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:3.5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:de9d498fa3566e7644e9e80eb937f7a652c837f32a79c0e21c95b32428735df0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243092953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e4a818d3cc1d1a88e6a5ca11f0ad4f310e93d17b9f08d104c4ceee0713a6c8`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:56 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:21 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:27:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 30 Jul 2020 23:56:23 GMT
ENV NEO4J_SHA256=29d7a205c27f786413abd61c462ddd67ab888042275a0f753a4912c49b501b5e NEO4J_TARBALL=neo4j-enterprise-3.5.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Thu, 30 Jul 2020 23:56:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.20-unix.tar.gz
# Thu, 30 Jul 2020 23:56:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.20-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 30 Jul 2020 23:56:24 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Thu, 30 Jul 2020 23:56:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-3.5.20-unix.tar.gz
RUN apt update      && apt install -y curl wget gosu jq      && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini      && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet      && chmod +x /sbin/tini      && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}      && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet      && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib      && mv /var/lib/neo4j-* "${NEO4J_HOME}"      && rm ${NEO4J_TARBALL}      && mv "${NEO4J_HOME}"/data /data      && mv "${NEO4J_HOME}"/logs /logs      && chown -R neo4j:neo4j /data      && chmod -R 777 /data      && chown -R neo4j:neo4j /logs      && chmod -R 777 /logs      && chown -R neo4j:neo4j "${NEO4J_HOME}"      && chmod -R 777 "${NEO4J_HOME}"      && ln -s /data "${NEO4J_HOME}"/data      && ln -s /logs "${NEO4J_HOME}"/logs      && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json      && rm -rf /tmp/*      && rm -rf /var/lib/apt/lists/*      && apt-get -y purge --auto-remove curl
# Thu, 30 Jul 2020 23:56:42 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jul 2020 23:56:42 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Jul 2020 23:56:43 GMT
VOLUME [/data /logs]
# Thu, 30 Jul 2020 23:56:43 GMT
COPY file:147c5d83a0e8f980042daf6c2540b40e96c165ebd51786a8d7697f8c1cd0cbc1 in /docker-entrypoint.sh 
# Thu, 30 Jul 2020 23:56:43 GMT
EXPOSE 7473 7474 7687
# Thu, 30 Jul 2020 23:56:43 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Thu, 30 Jul 2020 23:56:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b6b4d80d14aa8b600f13f69380464f034c5bd55aa583b15ada4f99439fd93`  
		Last Modified: Wed, 22 Jul 2020 22:48:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec391b2154add880db1ac8c314d9c05ca375d604f02cc1b1fcc9f93a4e78df`  
		Last Modified: Thu, 30 Jul 2020 22:29:58 GMT  
		Size: 40.6 MB (40610255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232f69f3145c170f151f9cc44dcd367008be0d140ea1be8c30d6555a04fcdf67`  
		Last Modified: Fri, 31 Jul 2020 00:11:25 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6496262f4379818071e7e0c0dbba2233a2d6f8b2e77d7b796cb4a42f1bcccd9`  
		Last Modified: Fri, 31 Jul 2020 00:11:25 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10994a8b879e82d692f14d393620db6d0c293a2ecba3d813048bc34ccf28460b`  
		Last Modified: Fri, 31 Jul 2020 00:11:37 GMT  
		Size: 172.1 MB (172127795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d76911747985921148e5096079586196406dd90e60bb0f24cf3f279f9ae2f3`  
		Last Modified: Fri, 31 Jul 2020 00:11:25 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0`

```console
$ docker pull neo4j@sha256:9df4769b4862e5f7232a1091cd34e8ee2f5338eb9078bf9f4822416993fff6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0` - linux; amd64

```console
$ docker pull neo4j@sha256:f1c20cb677e45b613cc8b994d8e89d6b47e1b819c34b21761283ebad7c06c6f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335159905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07dddb8902a8fba2af882c25fd702c4da414fc1e0d911637bfcf392ac6706dd`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:47:23 GMT
ENV NEO4J_SHA256=95738119ccc2f6518cc9f57295acf7560dbf90473c87d006d6b508d1971f1b46 NEO4J_TARBALL=neo4j-community-4.0.7-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:47:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.7-unix.tar.gz
# Wed, 29 Jul 2020 03:47:23 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:47:24 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:47:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.7-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:47:25 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:47:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.7-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:47:39 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:47:39 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:47:39 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:47:39 GMT
COPY file:05dba9ba87d60b4e0263eb5879419897896d9795d170348e7f8e2d62dbd96c1d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:47:39 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:47:40 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:47:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e6ce5dd990218c8dd736c70df2d2929698d2c472aa16450e6420e2b5bfb4f8`  
		Last Modified: Wed, 29 Jul 2020 04:09:09 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b8d3cafeed29f2f0a96869431541d16086c274167655f1aa6390d6583762a4`  
		Last Modified: Wed, 29 Jul 2020 04:09:09 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1e734b9e7d3896c44d573fc12bc82a5f6326628904962f7d971caf588cba2`  
		Last Modified: Wed, 29 Jul 2020 04:09:17 GMT  
		Size: 108.3 MB (108276424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f22c2fd3f5be00bb94b9e5b893c15a885e88f47c8023f4eb21a8cd9d172586`  
		Last Modified: Wed, 29 Jul 2020 04:09:10 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.0`

```console
$ docker pull neo4j@sha256:aa13d30bcb8fe57e7b6ef7fb8a69c29a069628cf3ecd099f6fa16a8ec72de26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.0` - linux; amd64

```console
$ docker pull neo4j@sha256:a8184a756605ded3b91f1423a7929a3524b5883513a8aa3918329bc5b19e4ece
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.0 MB (357960469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4618d159881d9240f97872ac728ef3058819f3edca46ea88ce3125641516631c`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:52:44 GMT
ENV NEO4J_SHA256=63c85ee709916f9f5fa2fac7274f1a55bdd44d6ab353cbdd05f050aed9532e82 NEO4J_TARBALL=neo4j-community-4.0.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:52:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.0-unix.tar.gz
# Wed, 29 Jul 2020 03:52:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.0-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:52:46 GMT
COPY multi:1bd8b938243645019f0ce38b6c9eeda97edd652b6f36f34befd360fa818b53e9 in /tmp/ 
# Wed, 29 Jul 2020 03:52:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.0-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:52:58 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:52:58 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:52:58 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:52:58 GMT
COPY file:c841ea3ded595df832d5ef9cc6bd4500806b0225676ea4550413353a0f0b82a5 in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:52:59 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:52:59 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:52:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a2846137e5747f51bd587471d0bda45607b17dc98bbda4fad12bd8ea926731`  
		Last Modified: Wed, 29 Jul 2020 04:11:52 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cde301b5915747d5638af2c403877f350e851b20d4004a573a5b2655d484bc`  
		Last Modified: Wed, 29 Jul 2020 04:11:52 GMT  
		Size: 426.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa81bffc630ebc13cacf767c6859186d395c2254e8585b38f4969c19356516f`  
		Last Modified: Wed, 29 Jul 2020 04:12:01 GMT  
		Size: 131.1 MB (131079241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaf231dc1604a6dce5f4d90cb995bd2ec772ee9be52b7976c4a8faf285f8382`  
		Last Modified: Wed, 29 Jul 2020 04:11:52 GMT  
		Size: 6.1 KB (6074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.0-enterprise`

```console
$ docker pull neo4j@sha256:39d70321e0d149a61f67f683eefad85f3bfa96fedc088a6a629f98b66297cdf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d9306156e9ec184835161382df4f25b020a4265afd5aac8dd2605509cc89854c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 MB (388200384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1150d7f6d060fa7e6f8d9868dd418a74fe68b578b9f68a4e45afa9ea293fb3a0`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:53:03 GMT
ENV NEO4J_SHA256=97060ce09086fa089516a2a3581b3db0d3d0dc4d2dd60daa470fa9ba090a7184 NEO4J_TARBALL=neo4j-enterprise-4.0.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:53:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.0-unix.tar.gz
# Wed, 29 Jul 2020 03:53:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.0-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:53:04 GMT
COPY multi:1bd8b938243645019f0ce38b6c9eeda97edd652b6f36f34befd360fa818b53e9 in /tmp/ 
# Wed, 29 Jul 2020 03:53:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.0-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:53:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:53:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:53:21 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:53:21 GMT
COPY file:c841ea3ded595df832d5ef9cc6bd4500806b0225676ea4550413353a0f0b82a5 in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:53:22 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:53:22 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:53:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c213a0db542ad2661effc882a84e52161dbab50e1f100d3662d070e1e44b24`  
		Last Modified: Wed, 29 Jul 2020 04:12:06 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde518c60d94e9cb2a5d8d270faa94a5197dec84ce08699e2942fc148e1b85c0`  
		Last Modified: Wed, 29 Jul 2020 04:12:06 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ef47b0b910281c2b712c06cf4f2ebaf1e2b20ef07cfdda21ca58d9b0f01a7b`  
		Last Modified: Wed, 29 Jul 2020 04:12:16 GMT  
		Size: 161.3 MB (161319152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581ff4cf2c7e14cb02997089f18405d4ef3e05e5a8f32f662b63182a7bf28ac9`  
		Last Modified: Wed, 29 Jul 2020 04:12:06 GMT  
		Size: 6.1 KB (6075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.1`

```console
$ docker pull neo4j@sha256:4a990d28628f0ac0d8f2d4bc12dcc9eab7aa7ac603b743f48cc791b05d2a7c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.1` - linux; amd64

```console
$ docker pull neo4j@sha256:605062bf41980df0ead837dfc3daae758ae8e5c4bd7c123ec2d79911a688c756
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333699968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e01808ff706b7de8221402b7e1b3cee9b3384b393c23cdf7ad5d75d7cce8f3`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:51:57 GMT
ENV NEO4J_SHA256=623c807ec23ed5c5e8db665a36bcdcb03a11ca2179ce24b61b220ecac60ace90 NEO4J_TARBALL=neo4j-community-4.0.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:51:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.1-unix.tar.gz
# Wed, 29 Jul 2020 03:51:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.1-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:51:59 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Wed, 29 Jul 2020 03:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.1-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:52:13 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:52:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:52:14 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:52:14 GMT
COPY file:180882cf912cbd895c07318211915dd64e94178cf2bd8093fdaf8e8c1b4692f3 in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:52:14 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:52:14 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:52:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e17bddf107472759740b9fc7092125fcf256efda18f5fea36f5149207982b1`  
		Last Modified: Wed, 29 Jul 2020 04:11:30 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9fbf6dc045cc6d3aa924eca13f08f500c230f8aa4762dd5f583e74d51181ca`  
		Last Modified: Wed, 29 Jul 2020 04:11:29 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba227944633876dabe311c90d56c13773cce46170f840ebb8950097a1ea7ab6`  
		Last Modified: Wed, 29 Jul 2020 04:11:36 GMT  
		Size: 106.8 MB (106818701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f4674a7481eb8fd5ef4e0b39b39b700c777ca5861b36edbea2aef22c2bf532`  
		Last Modified: Wed, 29 Jul 2020 04:11:30 GMT  
		Size: 6.1 KB (6085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.1-enterprise`

```console
$ docker pull neo4j@sha256:f81b3024e69713d9a279610bc9ea1189ee99c576e9d3eb446b1c7586e44d3bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ca024d44375814bc3318bc91a1b8d7bee132a42f8aade0398648deda45ab63f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (363977388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ec44ae51ff2f5bd893469133f5f222738868d488146ffd604c545c11203903`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:52:19 GMT
ENV NEO4J_SHA256=8c6aed4f05246a494ca5ec282f8fd7b4d8342c55adfd3dfa474b4e474f19fe09 NEO4J_TARBALL=neo4j-enterprise-4.0.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:52:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.1-unix.tar.gz
# Wed, 29 Jul 2020 03:52:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.1-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:52:21 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Wed, 29 Jul 2020 03:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.1-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:52:36 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:52:36 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:52:37 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:52:37 GMT
COPY file:180882cf912cbd895c07318211915dd64e94178cf2bd8093fdaf8e8c1b4692f3 in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:52:37 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:52:37 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87719caf7008723789c7ced4e52277d3fbaa7aaf4f303f2b73e63ed48422c5c2`  
		Last Modified: Wed, 29 Jul 2020 04:11:41 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fab2d8b8b199cfdd14b44845901a82655838b487bb95e666f815e8fb407636`  
		Last Modified: Wed, 29 Jul 2020 04:11:41 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84ab1e9a61822e45891249ebe5b550f0a4da0b3a034fcfbfdaed251b221fa95`  
		Last Modified: Wed, 29 Jul 2020 04:11:49 GMT  
		Size: 137.1 MB (137096121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0f43f8f2b4c28b3b7fc3ed0b3fde998ccef18aaba68e39274211c469f5f7c9`  
		Last Modified: Wed, 29 Jul 2020 04:11:41 GMT  
		Size: 6.1 KB (6085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.2`

```console
$ docker pull neo4j@sha256:266ea6856f9b3a2b06313ce609e2f33ba893079ce7a93b7534f143495816bf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.2` - linux; amd64

```console
$ docker pull neo4j@sha256:0dd9834961c57b7d742fb119108552c58cc5dccc2bf9f828e9ec3c9394816697
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333745138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2db61f5824e80c92b2753e62034fd29e2cde481cbd31ae84fef2342ac1fef4`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:51:13 GMT
ENV NEO4J_SHA256=e189f557a41835170fae42ee8d2dea9a94a3c790cfc73f0d9eb28be21b806830 NEO4J_TARBALL=neo4j-community-4.0.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:51:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.2-unix.tar.gz
# Wed, 29 Jul 2020 03:51:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.2-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:51:15 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Wed, 29 Jul 2020 03:51:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.2-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:51:26 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:51:27 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:51:27 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:51:27 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:51:27 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:51:27 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:51:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c1250f827b1c214369d9de0cb0acd99e3fafced97ea9f8cf3d9d93ff97cd4a`  
		Last Modified: Wed, 29 Jul 2020 04:11:07 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c332f841c1e6f1b1416668679f2c0244f6d8be27cc7fe955a07274955898d9`  
		Last Modified: Wed, 29 Jul 2020 04:11:07 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558e401c250005c17088c82dba6ccae26f697b10dd352ec34315a3da861cabd9`  
		Last Modified: Wed, 29 Jul 2020 04:11:14 GMT  
		Size: 106.9 MB (106864122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407bc5ce059ffa1e2da90eede1287957f83cc4057902ac324641b646c1d92f5e`  
		Last Modified: Wed, 29 Jul 2020 04:11:07 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.2-enterprise`

```console
$ docker pull neo4j@sha256:15c47dd6a9177aafc37e4a80749de99a5be89b1d93498792c6e9aafada20070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.2-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:96f5e11df727089ddceafe5f556e4d72e7e66a6f0fc629d4a306895403c732fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (364044081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ea5e9609ca5646ef5a2fd593f9b1c237dc2e730ee6cb269607f81c4a112f66`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:51:32 GMT
ENV NEO4J_SHA256=a39791336692e0cabb06f725b9f76dda43c80ef0d8073d696fea8feb5ee502f4 NEO4J_TARBALL=neo4j-enterprise-4.0.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:51:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.2-unix.tar.gz
# Wed, 29 Jul 2020 03:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.2-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:51:33 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Wed, 29 Jul 2020 03:51:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.2-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:51:50 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:51:50 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:51:50 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:51:50 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:51:51 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:51:51 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:51:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a8e7ff83416418944c3dc256a2a94d63045cdc933d0f10240401b3d60c18f9`  
		Last Modified: Wed, 29 Jul 2020 04:11:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a60dd32889168f59c71db94fa1730d2105c62ec5845dc06495140c6895a922`  
		Last Modified: Wed, 29 Jul 2020 04:11:18 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa499b8efdb7f51610866fe5808d51364c5d2b11f206330725b38ecbbc8bc90c`  
		Last Modified: Wed, 29 Jul 2020 04:11:26 GMT  
		Size: 137.2 MB (137163064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a57f6b7fb82a37606e5a93be59525929547a8e69b3159325c5f550de38ca22f`  
		Last Modified: Wed, 29 Jul 2020 04:11:17 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.3`

```console
$ docker pull neo4j@sha256:4f8040c007afa7138725d18b06ee9b94581e614d17c9ad5e6c7a12699154b698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.3` - linux; amd64

```console
$ docker pull neo4j@sha256:098c23b2737b6850cd30051736e9d53db482fe60b1f080d0e7518acf492e7b5e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.8 MB (333794964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9214b9f882892e072df96e283e019311e838a4eb6c7446d9d8644d81bec00a29`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:50:27 GMT
ENV NEO4J_SHA256=34db8c51899eced35ca5b9ba764649419f160b944b81abc52ed3587492c07085 NEO4J_TARBALL=neo4j-community-4.0.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:50:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
# Wed, 29 Jul 2020 03:50:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:50:28 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Wed, 29 Jul 2020 03:50:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.3-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:50:43 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:50:44 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:50:44 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:50:44 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:50:44 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:50:44 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:50:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd253077e67a9667239b26cfe6bf037c1aaac3a8fab84922853efce20aaced`  
		Last Modified: Wed, 29 Jul 2020 04:10:44 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b547825b7d29db184ab4342a9b8f43dcb64ddef9b20e15c61f5263194e2511`  
		Last Modified: Wed, 29 Jul 2020 04:10:44 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560991410fdc8b46785ff17ee8a3213e9729b20f399959621aa8e9fd55d4597f`  
		Last Modified: Wed, 29 Jul 2020 04:10:51 GMT  
		Size: 106.9 MB (106913948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ac1f592743884fb8cbaf372b43a96c8ce8587aafdc4fa797d0aa62b03ca335`  
		Last Modified: Wed, 29 Jul 2020 04:10:44 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.3-enterprise`

```console
$ docker pull neo4j@sha256:a8023ff86e6bc2f3abbf362aa6a1356dcf88c19af93ed14ea57be47078a4cc49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:bada0d21d8419f4b3582517261382f82a642dc9298bc5f4b99b36a8a8a548824
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364096179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4539f2bb02ffee24ce61bf0c4a7ed845cffca32bb7433c67c4d25baa90a059`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:50:48 GMT
ENV NEO4J_SHA256=f70ea236b75d4210a49ff4e009388cc99577d50a38eb25ac73fce16eee783aa0 NEO4J_TARBALL=neo4j-enterprise-4.0.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:50:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
# Wed, 29 Jul 2020 03:50:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:50:50 GMT
COPY multi:5d2171ebdeb5752d080b96f9ac9e7cf87aeb5949ca626a75789d79e846b648b2 in /tmp/ 
# Wed, 29 Jul 2020 03:51:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.3-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:51:06 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:51:06 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:51:06 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:51:06 GMT
COPY file:2ee670821c25faddd6488b3c5db5184559d53b25bcb108162fb216e902abb8bc in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:51:07 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:51:07 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:51:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27ebebc7561eb0078db556feac9ea18d8c67ad1233e68514197a00a1f375873`  
		Last Modified: Wed, 29 Jul 2020 04:10:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd93e7d80e01a9afd20759c4a17039b8393b705026c2d8bce625dae534c503`  
		Last Modified: Wed, 29 Jul 2020 04:10:55 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b5ca7c87927f190902f949b1327b56ecc6c1c53270858c5ec76ecd24eda842`  
		Last Modified: Wed, 29 Jul 2020 04:11:03 GMT  
		Size: 137.2 MB (137215162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0c7cd0022d356c02f0be660d86e2839c2d2366874549305c9b0d61de6f7382`  
		Last Modified: Wed, 29 Jul 2020 04:10:55 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.4`

```console
$ docker pull neo4j@sha256:3be874af7d8224c50c91c8cd0cd5cba3ccca6ce8a1f236c88f7cbb03ca08ed75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.4` - linux; amd64

```console
$ docker pull neo4j@sha256:dbfa6cf3784f01f6c5f45d3f518866b52196bce11da86c34a1f7bd8fa9b5b409
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.9 MB (333920678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25962ea2de7787a057fdf1ad07da2b9da1610e9e23ddede6475a8ce18e819793`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:49:40 GMT
ENV NEO4J_SHA256=e467b30f483132e62be0288f7db337148cea25221a80e23dba8af995a03b60a3 NEO4J_TARBALL=neo4j-community-4.0.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:49:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.4-unix.tar.gz
# Wed, 29 Jul 2020 03:49:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.4-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:49:41 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:49:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.4-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:49:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:49:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:49:56 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:49:56 GMT
COPY file:a3b87f809eb056e613afeab88f27776bdd507a412d05df3bdf1a3b6d58082df3 in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:49:56 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:49:56 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:49:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995d7bd6464d5503ac949af2f4dee92513e294e9c4931c3722d464d1ef19ef15`  
		Last Modified: Wed, 29 Jul 2020 04:10:19 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270389a90f97985760f73e20de48437200ef43469284e2604e890323efd28794`  
		Last Modified: Wed, 29 Jul 2020 04:10:19 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc69f5bd64974f25525ef58db19ca14b5d812be843032582582b63d3f6161754`  
		Last Modified: Wed, 29 Jul 2020 04:10:26 GMT  
		Size: 107.0 MB (107039687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1019fe8c38c473ae25100102c659cfa85f4830c47b692d1ffa591acc00b26e`  
		Last Modified: Wed, 29 Jul 2020 04:10:19 GMT  
		Size: 5.8 KB (5763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.4-enterprise`

```console
$ docker pull neo4j@sha256:da80d5755db40288e61e3a97919fa5d6e155be0b75c62a3260d3009cf4ceb6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ee0f8c807da4e46c11f68596ede61132aa6ae37f514ecd79fde448ef9419cd5a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364209726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dbfb50bdf0a157344e8cde8612792d7bb0432b9dbc9d57c02e1e654f0d0ba7`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:50:01 GMT
ENV NEO4J_SHA256=c511128e00abc51feceaef2029c1a4d37af53b80d78621f98a788b56d9fc51ec NEO4J_TARBALL=neo4j-enterprise-4.0.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:50:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.4-unix.tar.gz
# Wed, 29 Jul 2020 03:50:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.4-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:50:03 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:50:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.4-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:50:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:50:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:50:19 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:50:19 GMT
COPY file:a3b87f809eb056e613afeab88f27776bdd507a412d05df3bdf1a3b6d58082df3 in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:50:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:50:19 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:50:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139bf733009c46c0ad911c8d0246c6ed44f1259c6fcf1069fddcb5ce7b0ad115`  
		Last Modified: Wed, 29 Jul 2020 04:10:32 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93dbb48d54f855a3c12584b354e8b9aed9519ee518f2c74eeb918b1bc83c635`  
		Last Modified: Wed, 29 Jul 2020 04:10:32 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cce997aaf3d0fb54a3c9e252f428b5ccba6c1049e269c0da41f031ae587b836`  
		Last Modified: Wed, 29 Jul 2020 04:10:40 GMT  
		Size: 137.3 MB (137328736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f2a5a1d0c50ca2cfbc61ff1e0a48b807b2b23b8952f51833bcdc3f7a9c83d`  
		Last Modified: Wed, 29 Jul 2020 04:10:32 GMT  
		Size: 5.8 KB (5763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.5`

```console
$ docker pull neo4j@sha256:a9ed0301ae718de687458249b092e2aab7ed8f10b0431de5d7c6c656e719f31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.5` - linux; amd64

```console
$ docker pull neo4j@sha256:e01697b42865c214c13b780c8f50606625b41e158fddfd6668c8d60838b4a303
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.9 MB (333928491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc31abd40ee1bac0ee7d957049cb91d124a1dc1b3d0444a48a22e87de531df`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:48:53 GMT
ENV NEO4J_SHA256=7f3c17b4d33d0cbda0d2bce2e48ee0ede06d948ed0fd1b7bf64b6a00d858c93f NEO4J_TARBALL=neo4j-community-4.0.5-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:48:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.5-unix.tar.gz
# Wed, 29 Jul 2020 03:48:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.5-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:48:54 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:49:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.5-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:49:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:49:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:49:09 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:49:09 GMT
COPY file:05dba9ba87d60b4e0263eb5879419897896d9795d170348e7f8e2d62dbd96c1d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:49:09 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:49:09 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:49:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ad846ce5a012e63dd069e791940b76458b9e5fb6edf4ef5088507948dc3e52`  
		Last Modified: Wed, 29 Jul 2020 04:09:55 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2c86680d44aee045e969279a176ce8847a9ddc57f0a5ef7aac03cadfca960b`  
		Last Modified: Wed, 29 Jul 2020 04:09:55 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd6045a97c7603503f5e88fb4e8b52223c66d3518a384b31d40aeab001c4bf7`  
		Last Modified: Wed, 29 Jul 2020 04:10:02 GMT  
		Size: 107.0 MB (107047510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a40a93c5f0e09492bb3393cc06c05f8a3b7c714fa555e278737379aa278c13`  
		Last Modified: Wed, 29 Jul 2020 04:09:54 GMT  
		Size: 5.8 KB (5753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.5-enterprise`

```console
$ docker pull neo4j@sha256:7cfb306eba6bc62f88af4bc065d803de11a3499289e6eb7da28a8265771014e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:71f818932ff7b6f71d6ebeea644cbd9be33ec9ccc720f20bd3f51f2382f6c694
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364220066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbef2b03fd4edca665076deb28fc0b32d70601f131d3be6ba24866e99d2a159`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:49:15 GMT
ENV NEO4J_SHA256=b388b0d55f230154278471a4116ca3de7280d17dda69fa5d766acda42b25886a NEO4J_TARBALL=neo4j-enterprise-4.0.5-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:49:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.5-unix.tar.gz
# Wed, 29 Jul 2020 03:49:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.5-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:49:16 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:49:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.5-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:49:32 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:49:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:49:33 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:49:33 GMT
COPY file:05dba9ba87d60b4e0263eb5879419897896d9795d170348e7f8e2d62dbd96c1d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:49:33 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:49:33 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:49:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3366b4f779ca324be9a87f8bbb1e5a73e9ae2d4ae60c01af793b5777a64b04`  
		Last Modified: Wed, 29 Jul 2020 04:10:07 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1391ed76217c8e921221f79f8189cd3c6375c1dc20d265dee8d439d9ab169c59`  
		Last Modified: Wed, 29 Jul 2020 04:10:06 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90bc43931b533ae07d0b1f003bc93a18e2f43d0a78410a8ba421c255fa249d3`  
		Last Modified: Wed, 29 Jul 2020 04:10:15 GMT  
		Size: 137.3 MB (137339087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4df1f9e96fa450344ca5a8c1e4e3a75358d032d66a1650151dadb0bf3443a94`  
		Last Modified: Wed, 29 Jul 2020 04:10:06 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.6`

```console
$ docker pull neo4j@sha256:c3040dda8b6f04d4897ee1c830e89077114871e1ce3467ad1437d4de25672c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.6` - linux; amd64

```console
$ docker pull neo4j@sha256:ea35f3681e53a3bc6e7297c8b9f9618aaf25de72fdc917bc93ace69f6dcdd55f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333957465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ac56ff7f21e8d1202576fabfb076035f10b83da8fa080482318ae9dcf9b7a2`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:48:10 GMT
ENV NEO4J_SHA256=47a7edfe0f673517c7c21b33b5f124377cbfa1763081475ba1013caa6ad2340e NEO4J_TARBALL=neo4j-community-4.0.6-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.6-unix.tar.gz
# Wed, 29 Jul 2020 03:48:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.6-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:48:11 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:48:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.6-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:48:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:48:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:48:25 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:48:25 GMT
COPY file:05dba9ba87d60b4e0263eb5879419897896d9795d170348e7f8e2d62dbd96c1d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:48:26 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:48:26 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:48:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945960009d8b5b0e2811d61067524ec2a83aa08fef5d6c94ec1f034988699e35`  
		Last Modified: Wed, 29 Jul 2020 04:09:33 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fbd66d24e7d50282dbca5d8350e76988120de69fe3ae15b922ad20bc4893f5`  
		Last Modified: Wed, 29 Jul 2020 04:09:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a340648d0a75cfdcd79b2cc3060173f0ca7867c2db02f7d9722f6466572581`  
		Last Modified: Wed, 29 Jul 2020 04:09:40 GMT  
		Size: 107.1 MB (107076486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8347e257f4ee8296daa81ab481b43fa42a37e7d887f0218bd1184e9c602b5c54`  
		Last Modified: Wed, 29 Jul 2020 04:09:33 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.6-enterprise`

```console
$ docker pull neo4j@sha256:629f6dddbba7745b13f6d5cfe283a7882c596c727e513431bc0aaf0d9cb4a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.6-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6d0dd2dd2f0f8d2d996d3d59ef5e8b3a0fac8b346217ed21f071663909026397
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364241260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4f7ee502b6f503272ba41343dbada2a450f753a2109908a3876a34bcbc52ab`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:48:31 GMT
ENV NEO4J_SHA256=69c34e96c4e1f6ac2ea1a7d1a5b78e02f3624c1d3b0ed6476eee04cab15cae0c NEO4J_TARBALL=neo4j-enterprise-4.0.6-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:48:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.6-unix.tar.gz
# Wed, 29 Jul 2020 03:48:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.6-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:48:32 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:48:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.6-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:48:48 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:48:48 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:48:48 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:48:49 GMT
COPY file:05dba9ba87d60b4e0263eb5879419897896d9795d170348e7f8e2d62dbd96c1d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:48:49 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:48:49 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:48:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd34f5edb10a1c19a7c7be2a87236719d2fba4f497feb0ce42fa056b6a1169fa`  
		Last Modified: Wed, 29 Jul 2020 04:09:43 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c72b9ce683fc69f1339ad8d1ba57bb49501ac64fb19d78344e48dfaaca12dff`  
		Last Modified: Wed, 29 Jul 2020 04:09:43 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dd4c99af1ea1d662ded8b309b8009c4fac7a634003fd36fb54bd501e4421fe`  
		Last Modified: Wed, 29 Jul 2020 04:09:51 GMT  
		Size: 137.4 MB (137360281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadbae83dd6b0b6cb5996b939780e65fa2a57423be4321b5845691f57f6ab72e`  
		Last Modified: Wed, 29 Jul 2020 04:09:43 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.7`

```console
$ docker pull neo4j@sha256:9df4769b4862e5f7232a1091cd34e8ee2f5338eb9078bf9f4822416993fff6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.7` - linux; amd64

```console
$ docker pull neo4j@sha256:f1c20cb677e45b613cc8b994d8e89d6b47e1b819c34b21761283ebad7c06c6f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335159905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07dddb8902a8fba2af882c25fd702c4da414fc1e0d911637bfcf392ac6706dd`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:47:23 GMT
ENV NEO4J_SHA256=95738119ccc2f6518cc9f57295acf7560dbf90473c87d006d6b508d1971f1b46 NEO4J_TARBALL=neo4j-community-4.0.7-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:47:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.7-unix.tar.gz
# Wed, 29 Jul 2020 03:47:23 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:47:24 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:47:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.7-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:47:25 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:47:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.0.7-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:47:39 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:47:39 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:47:39 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:47:39 GMT
COPY file:05dba9ba87d60b4e0263eb5879419897896d9795d170348e7f8e2d62dbd96c1d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:47:39 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:47:40 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:47:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e6ce5dd990218c8dd736c70df2d2929698d2c472aa16450e6420e2b5bfb4f8`  
		Last Modified: Wed, 29 Jul 2020 04:09:09 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b8d3cafeed29f2f0a96869431541d16086c274167655f1aa6390d6583762a4`  
		Last Modified: Wed, 29 Jul 2020 04:09:09 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1e734b9e7d3896c44d573fc12bc82a5f6326628904962f7d971caf588cba2`  
		Last Modified: Wed, 29 Jul 2020 04:09:17 GMT  
		Size: 108.3 MB (108276424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f22c2fd3f5be00bb94b9e5b893c15a885e88f47c8023f4eb21a8cd9d172586`  
		Last Modified: Wed, 29 Jul 2020 04:09:10 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0.7-enterprise`

```console
$ docker pull neo4j@sha256:9cd609e226619b567569c0f9fd8b4c3d749d6283ca1f0a1a4d71e8df05ebb43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0.7-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:f5722aa88d7766a792b3ed92e1248c9cbaa1d5972b9a16f0f42e3786136cad6d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365539268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735385a47402373167251431b570d7c53b3b76df25c76e431e7513db001c5c8`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:47:44 GMT
ENV NEO4J_SHA256=975476bdd11c466769e5cd34e6bac85b43a29f1ccda8a5da8b764a71d752641c NEO4J_TARBALL=neo4j-enterprise-4.0.7-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:47:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.7-unix.tar.gz
# Wed, 29 Jul 2020 03:47:45 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:47:45 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:47:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.7-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:47:46 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:48:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.7-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:48:02 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:48:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:48:02 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:48:03 GMT
COPY file:05dba9ba87d60b4e0263eb5879419897896d9795d170348e7f8e2d62dbd96c1d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:48:03 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:48:03 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bea682287e5bf7d6a5c7ddddb406fe66060c188880ae662a3b2c8729ee21edc`  
		Last Modified: Wed, 29 Jul 2020 04:09:20 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4139ee4700712d3e5979620306b89ced8c9299c15cd0b1647907547ccc185a`  
		Last Modified: Wed, 29 Jul 2020 04:09:20 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aee418627484efee6ca8f6a97fae9cc0804e0d0a9fbe269aa84a304e0389d1`  
		Last Modified: Wed, 29 Jul 2020 04:09:29 GMT  
		Size: 138.7 MB (138655789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97afb23724c4c9bda62053ee306594692d5fd53d64e6244161a3849ef1b0300`  
		Last Modified: Wed, 29 Jul 2020 04:09:20 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.0-enterprise`

```console
$ docker pull neo4j@sha256:9cd609e226619b567569c0f9fd8b4c3d749d6283ca1f0a1a4d71e8df05ebb43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:f5722aa88d7766a792b3ed92e1248c9cbaa1d5972b9a16f0f42e3786136cad6d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365539268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735385a47402373167251431b570d7c53b3b76df25c76e431e7513db001c5c8`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:47:44 GMT
ENV NEO4J_SHA256=975476bdd11c466769e5cd34e6bac85b43a29f1ccda8a5da8b764a71d752641c NEO4J_TARBALL=neo4j-enterprise-4.0.7-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:47:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.7-unix.tar.gz
# Wed, 29 Jul 2020 03:47:45 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:47:45 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:47:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.7-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:47:46 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:48:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.0.7-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:48:02 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:48:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:48:02 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:48:03 GMT
COPY file:05dba9ba87d60b4e0263eb5879419897896d9795d170348e7f8e2d62dbd96c1d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:48:03 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:48:03 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bea682287e5bf7d6a5c7ddddb406fe66060c188880ae662a3b2c8729ee21edc`  
		Last Modified: Wed, 29 Jul 2020 04:09:20 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4139ee4700712d3e5979620306b89ced8c9299c15cd0b1647907547ccc185a`  
		Last Modified: Wed, 29 Jul 2020 04:09:20 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aee418627484efee6ca8f6a97fae9cc0804e0d0a9fbe269aa84a304e0389d1`  
		Last Modified: Wed, 29 Jul 2020 04:09:29 GMT  
		Size: 138.7 MB (138655789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97afb23724c4c9bda62053ee306594692d5fd53d64e6244161a3849ef1b0300`  
		Last Modified: Wed, 29 Jul 2020 04:09:20 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.1`

```console
$ docker pull neo4j@sha256:c68386ae810dbe6023a42ab0ff1eb5b4a795edd7ff7148e8f749e923c158e91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.1` - linux; amd64

```console
$ docker pull neo4j@sha256:14e79caf61c6151023b7862c8eaf254882730ece2cf29b79d957932fd933504d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348433217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95528ad6afe614bc37f65926ebf9ff50c5846bcbba70f562f92a8891547a56a1`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:45:59 GMT
ENV NEO4J_SHA256=4f663a520bec40dfd0b1972feb3cf93af321c230b448adb6dc917717e67a1271 NEO4J_TARBALL=neo4j-community-4.1.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:45:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz
# Wed, 29 Jul 2020 03:45:59 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:45:59 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:46:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:46:00 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:46:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:46:13 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:46:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:46:13 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:46:13 GMT
COPY file:8b8c5515388aee21603a6091dadc2d3a6d4f7790a45cecce25e8ef5ed92f530d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:46:13 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:46:13 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:46:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce5c537cb002af6377e5ac780158a0ea666c3871b31ee00e741ade8a7297a6b`  
		Last Modified: Wed, 29 Jul 2020 04:08:19 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384a9055d5d43ec7ce8e153325992d83f57d0493a8a9d15bb5b825b82405031`  
		Last Modified: Wed, 29 Jul 2020 04:08:18 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94658afdfe631d1c39676b2f6bbc8dbc35035415b6c24a45499767688b6c38d`  
		Last Modified: Wed, 29 Jul 2020 04:08:26 GMT  
		Size: 121.5 MB (121549627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86422ad989135e39aa731b8273233d803f96a092f7937ff4578108a4b5e4f8b9`  
		Last Modified: Wed, 29 Jul 2020 04:08:18 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.1.0`

```console
$ docker pull neo4j@sha256:bb0a35855449b712d5b98f9f64cc55df7d6a0523d4c643fd9a3534c4eae78aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.1.0` - linux; amd64

```console
$ docker pull neo4j@sha256:5af788ee1f294bb9131e3ce2069afb0bedc8e358e3365ff797052d206fe8707d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336905656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e029069b4dddce3b66c2b256bf873a3b340ca1b38bc424428700cc5c27166a`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:46:40 GMT
ENV NEO4J_SHA256=b598edeb3401e5ec40fb7bc3370307addfcaa21565f731016c9c7f8e70af659a NEO4J_TARBALL=neo4j-community-4.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:46:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.0-unix.tar.gz
# Wed, 29 Jul 2020 03:46:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.0-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:46:41 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:46:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.0-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:46:55 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:46:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:46:55 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:46:55 GMT
COPY file:8b8c5515388aee21603a6091dadc2d3a6d4f7790a45cecce25e8ef5ed92f530d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:46:55 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:46:56 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:46:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af383fc56bf3b8fe9e12e34a55e5a73598109cc252e1d6372ea1e64a5a3d90eb`  
		Last Modified: Wed, 29 Jul 2020 04:08:46 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8618ebd230b1408a55fd0e4427396de364593e8f8b572279e4938c8bd324f6da`  
		Last Modified: Wed, 29 Jul 2020 04:08:46 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b0ec0ccf6ce1555fc527727394b97366dc3d85eb0d72332e1c1f3fa9104b51`  
		Last Modified: Wed, 29 Jul 2020 04:08:53 GMT  
		Size: 110.0 MB (110024570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4011e9bffcb910e1fa041e5bcff22f3dcb05c1f78e8679f5189f5a746121eaf5`  
		Last Modified: Wed, 29 Jul 2020 04:08:46 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.1.0-enterprise`

```console
$ docker pull neo4j@sha256:06b7ced6958a5b5c137ed119b9c8a8e6feeec158d1d1784921c509f59ada0091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.1.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e34eebd880d7f73a66f62a595e1d1a1c6ed9bffd105dd2edd2a410c1ad834aa9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366598380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba35c1fd57d521601b410d081cbf863d0f0d9135d4af90e2476cc4289c744531`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:47:01 GMT
ENV NEO4J_SHA256=8ca612cf93432fefc256d54d5576e19d5f2267690b6130bd135a1741e7613123 NEO4J_TARBALL=neo4j-enterprise-4.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j TINI_VERSION=v0.18.0 TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:47:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.0-unix.tar.gz
# Wed, 29 Jul 2020 03:47:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.0-unix.tar.gz
RUN addgroup --system neo4j && adduser --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:47:02 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.0-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini" > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:47:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:47:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:47:18 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:47:18 GMT
COPY file:8b8c5515388aee21603a6091dadc2d3a6d4f7790a45cecce25e8ef5ed92f530d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:47:19 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:47:19 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:47:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaca9f3d4005ebc5b9e1d9513a626b651d69fb0be72794cd70002651182b54c`  
		Last Modified: Wed, 29 Jul 2020 04:08:58 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dd859210376df283b09745703f9ade3819fb67c9eeff2e263a761172898beb`  
		Last Modified: Wed, 29 Jul 2020 04:08:57 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf1fe96da9bcd739ea08612727f61085c7d7156dff68c00f854b4afd70dcfd`  
		Last Modified: Wed, 29 Jul 2020 04:09:06 GMT  
		Size: 139.7 MB (139717293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc1467f5ad6d2eb869723dc079cf223874552ada36570aa7ecc41de0caf289`  
		Last Modified: Wed, 29 Jul 2020 04:08:57 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.1.1`

```console
$ docker pull neo4j@sha256:c68386ae810dbe6023a42ab0ff1eb5b4a795edd7ff7148e8f749e923c158e91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.1.1` - linux; amd64

```console
$ docker pull neo4j@sha256:14e79caf61c6151023b7862c8eaf254882730ece2cf29b79d957932fd933504d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348433217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95528ad6afe614bc37f65926ebf9ff50c5846bcbba70f562f92a8891547a56a1`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:45:59 GMT
ENV NEO4J_SHA256=4f663a520bec40dfd0b1972feb3cf93af321c230b448adb6dc917717e67a1271 NEO4J_TARBALL=neo4j-community-4.1.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:45:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz
# Wed, 29 Jul 2020 03:45:59 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:45:59 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:46:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:46:00 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:46:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:46:13 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:46:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:46:13 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:46:13 GMT
COPY file:8b8c5515388aee21603a6091dadc2d3a6d4f7790a45cecce25e8ef5ed92f530d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:46:13 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:46:13 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:46:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce5c537cb002af6377e5ac780158a0ea666c3871b31ee00e741ade8a7297a6b`  
		Last Modified: Wed, 29 Jul 2020 04:08:19 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384a9055d5d43ec7ce8e153325992d83f57d0493a8a9d15bb5b825b82405031`  
		Last Modified: Wed, 29 Jul 2020 04:08:18 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94658afdfe631d1c39676b2f6bbc8dbc35035415b6c24a45499767688b6c38d`  
		Last Modified: Wed, 29 Jul 2020 04:08:26 GMT  
		Size: 121.5 MB (121549627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86422ad989135e39aa731b8273233d803f96a092f7937ff4578108a4b5e4f8b9`  
		Last Modified: Wed, 29 Jul 2020 04:08:18 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.1.1-enterprise`

```console
$ docker pull neo4j@sha256:5ebe576ae857e49d81749db155569203713b35290d01d8c7f5e00e3feadc522d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.1.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ce431d06a92602f8cf83aea46b79d872bd3afbe7682f693760bafeb499b8d9bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378191263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e73db9d0a63ae23b4f795237a8f9e939daefad2366943aa32e7c3b1ef961920`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:46:18 GMT
ENV NEO4J_SHA256=f1b5ee0db7771abeb7a9db2f3c8b6d92850d5587ed99926c417bf5c70d883c06 NEO4J_TARBALL=neo4j-enterprise-4.1.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:46:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz
# Wed, 29 Jul 2020 03:46:18 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:46:18 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:46:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:46:20 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:46:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:46:33 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:46:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:46:33 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:46:33 GMT
COPY file:8b8c5515388aee21603a6091dadc2d3a6d4f7790a45cecce25e8ef5ed92f530d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:46:34 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:46:34 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:46:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0208313bb4f06ec0077646a457155de63dba6f27a7bc7c3659cdd8e09cebd08`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6ef751d06ebbd70686c58916cae0769ef25818e69a6b669701042c8deafd49`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b81d7d441fb5d6154401133f8bf9309de5ff55f7b0a52dd7dea5f3ed59351b`  
		Last Modified: Wed, 29 Jul 2020 04:08:39 GMT  
		Size: 151.3 MB (151307676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69519abaccb24aea2363556f7074e3f023a50e1e2e56ad2e573f741f9c499d6c`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.1-enterprise`

```console
$ docker pull neo4j@sha256:5ebe576ae857e49d81749db155569203713b35290d01d8c7f5e00e3feadc522d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:4.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ce431d06a92602f8cf83aea46b79d872bd3afbe7682f693760bafeb499b8d9bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378191263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e73db9d0a63ae23b4f795237a8f9e939daefad2366943aa32e7c3b1ef961920`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:46:18 GMT
ENV NEO4J_SHA256=f1b5ee0db7771abeb7a9db2f3c8b6d92850d5587ed99926c417bf5c70d883c06 NEO4J_TARBALL=neo4j-enterprise-4.1.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:46:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz
# Wed, 29 Jul 2020 03:46:18 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:46:18 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:46:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:46:20 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:46:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:46:33 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:46:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:46:33 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:46:33 GMT
COPY file:8b8c5515388aee21603a6091dadc2d3a6d4f7790a45cecce25e8ef5ed92f530d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:46:34 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:46:34 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:46:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0208313bb4f06ec0077646a457155de63dba6f27a7bc7c3659cdd8e09cebd08`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6ef751d06ebbd70686c58916cae0769ef25818e69a6b669701042c8deafd49`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b81d7d441fb5d6154401133f8bf9309de5ff55f7b0a52dd7dea5f3ed59351b`  
		Last Modified: Wed, 29 Jul 2020 04:08:39 GMT  
		Size: 151.3 MB (151307676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69519abaccb24aea2363556f7074e3f023a50e1e2e56ad2e573f741f9c499d6c`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:5ebe576ae857e49d81749db155569203713b35290d01d8c7f5e00e3feadc522d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ce431d06a92602f8cf83aea46b79d872bd3afbe7682f693760bafeb499b8d9bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378191263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e73db9d0a63ae23b4f795237a8f9e939daefad2366943aa32e7c3b1ef961920`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:46:18 GMT
ENV NEO4J_SHA256=f1b5ee0db7771abeb7a9db2f3c8b6d92850d5587ed99926c417bf5c70d883c06 NEO4J_TARBALL=neo4j-enterprise-4.1.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:46:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz
# Wed, 29 Jul 2020 03:46:18 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:46:18 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:46:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:46:20 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:46:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:46:33 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:46:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:46:33 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:46:33 GMT
COPY file:8b8c5515388aee21603a6091dadc2d3a6d4f7790a45cecce25e8ef5ed92f530d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:46:34 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:46:34 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:46:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0208313bb4f06ec0077646a457155de63dba6f27a7bc7c3659cdd8e09cebd08`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6ef751d06ebbd70686c58916cae0769ef25818e69a6b669701042c8deafd49`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b81d7d441fb5d6154401133f8bf9309de5ff55f7b0a52dd7dea5f3ed59351b`  
		Last Modified: Wed, 29 Jul 2020 04:08:39 GMT  
		Size: 151.3 MB (151307676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69519abaccb24aea2363556f7074e3f023a50e1e2e56ad2e573f741f9c499d6c`  
		Last Modified: Wed, 29 Jul 2020 04:08:30 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:c68386ae810dbe6023a42ab0ff1eb5b4a795edd7ff7148e8f749e923c158e91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:14e79caf61c6151023b7862c8eaf254882730ece2cf29b79d957932fd933504d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348433217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95528ad6afe614bc37f65926ebf9ff50c5846bcbba70f562f92a8891547a56a1`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 22 Jul 2020 22:40:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:40:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 22 Jul 2020 22:40:33 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:29:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.8_10.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_11.0.8_10.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:29:24 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 03:45:59 GMT
ENV NEO4J_SHA256=4f663a520bec40dfd0b1972feb3cf93af321c230b448adb6dc917717e67a1271 NEO4J_TARBALL=neo4j-community-4.1.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 29 Jul 2020 03:45:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz
# Wed, 29 Jul 2020 03:45:59 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Wed, 29 Jul 2020 03:45:59 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Wed, 29 Jul 2020 03:46:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 29 Jul 2020 03:46:00 GMT
COPY multi:1191f2c2f6370a31e5ebabb252b693639097aaeb5d54b38b45698e028dab3756 in /tmp/ 
# Wed, 29 Jul 2020 03:46:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.1.1-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Wed, 29 Jul 2020 03:46:13 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 03:46:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 29 Jul 2020 03:46:13 GMT
VOLUME [/data /logs]
# Wed, 29 Jul 2020 03:46:13 GMT
COPY file:8b8c5515388aee21603a6091dadc2d3a6d4f7790a45cecce25e8ef5ed92f530d in /docker-entrypoint.sh 
# Wed, 29 Jul 2020 03:46:13 GMT
EXPOSE 7473 7474 7687
# Wed, 29 Jul 2020 03:46:13 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Wed, 29 Jul 2020 03:46:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b5d3bc409673c9f77720030b623cb2c26bda1203fbcca9734ebfe1c68f18d`  
		Last Modified: Wed, 22 Jul 2020 22:47:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b7c556cec2295da9cff0a9a2255703cb77792ad82f9e372b743d24f352e5`  
		Last Modified: Wed, 29 Jul 2020 01:37:03 GMT  
		Size: 196.5 MB (196526169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce5c537cb002af6377e5ac780158a0ea666c3871b31ee00e741ade8a7297a6b`  
		Last Modified: Wed, 29 Jul 2020 04:08:19 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384a9055d5d43ec7ce8e153325992d83f57d0493a8a9d15bb5b825b82405031`  
		Last Modified: Wed, 29 Jul 2020 04:08:18 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94658afdfe631d1c39676b2f6bbc8dbc35035415b6c24a45499767688b6c38d`  
		Last Modified: Wed, 29 Jul 2020 04:08:26 GMT  
		Size: 121.5 MB (121549627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86422ad989135e39aa731b8273233d803f96a092f7937ff4578108a4b5e4f8b9`  
		Last Modified: Wed, 29 Jul 2020 04:08:18 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
