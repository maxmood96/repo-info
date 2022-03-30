## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:dfc11d352e76a50343b4f53ff5900e695822fbc1e6d2009c97b4cc9749e2a8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c1ab00a8ef19725db33428a69a77586385b5e28be144c922d47931d8cb468788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.2 MB (448226658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5beac34e55a508b1e34181fc7df1a7c66000f1e56d7fe0c76f26cd9bb26edd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:55:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 29 Mar 2022 00:55:29 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 29 Mar 2022 00:55:29 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:55:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:55:29 GMT
ENV JAVA_VERSION=11.0.14.1
# Tue, 29 Mar 2022 00:55:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:55:56 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 02:51:23 GMT
ENV NEO4J_SHA256=c89c19d93db0bcb8e5eae36f1f56dab4e46f8b235b3f2605c64a8b9b4b32ba13 NEO4J_TARBALL=neo4j-enterprise-4.4.5-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 30 Mar 2022 02:51:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.5-unix.tar.gz
# Wed, 30 Mar 2022 02:51:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.5-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 30 Mar 2022 02:51:24 GMT
COPY multi:b3339e410120d82bf4e9d9934ea62d58e85e63f5685435dca318feb368d23c5a in /startup/ 
# Wed, 30 Mar 2022 02:51:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.5-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:51:39 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 02:51:39 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Mar 2022 02:51:40 GMT
VOLUME [/data /logs]
# Wed, 30 Mar 2022 02:51:40 GMT
EXPOSE 7473 7474 7687
# Wed, 30 Mar 2022 02:51:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:51:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dc05f270bad654ee17f1143c48586c188a72929a128d61fd8ae15905d7b00`  
		Last Modified: Tue, 29 Mar 2022 01:04:32 GMT  
		Size: 1.6 MB (1582122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b2c24c052eb115ae98ac01ea7a403af9bd678866744f0eea033d71d18f893b`  
		Last Modified: Tue, 29 Mar 2022 01:10:57 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313fb0b5de5ee7f8a750da20f5629882554fb425ee07ed611b8a934cb2506da5`  
		Last Modified: Tue, 29 Mar 2022 01:11:12 GMT  
		Size: 203.5 MB (203524269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b207306674ada5775c807cfa7d6b793bfb67548d7551d9a09bae8c305aca5`  
		Last Modified: Wed, 30 Mar 2022 03:25:37 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c54b353e0fd5248f4d0a714864d93a95e7459fa0d16f579e028df112d833c8`  
		Last Modified: Wed, 30 Mar 2022 03:25:37 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824405f61fdd6cd2eb84e1d03533c6fc5d8650c92776ea9398a78f0df0a79b0a`  
		Last Modified: Wed, 30 Mar 2022 03:25:47 GMT  
		Size: 211.7 MB (211730174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3294e7124fcc7f2733fb6496b606fff7760b2f1de09a5ac6ac286607e4c13733
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.8 MB (443757752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c254ef6e1bf88f8ec661379bdeb4ea3d3fa8a65c8875220ae2fe6c0dca1d7f09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 01:22:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 29 Mar 2022 01:22:58 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 29 Mar 2022 01:22:59 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 01:23:00 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 01:23:01 GMT
ENV JAVA_VERSION=11.0.14.1
# Tue, 29 Mar 2022 01:23:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:23:46 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 10:56:59 GMT
ENV NEO4J_SHA256=c89c19d93db0bcb8e5eae36f1f56dab4e46f8b235b3f2605c64a8b9b4b32ba13 NEO4J_TARBALL=neo4j-enterprise-4.4.5-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 30 Mar 2022 10:56:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.5-unix.tar.gz
# Wed, 30 Mar 2022 10:57:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.5-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 30 Mar 2022 10:57:02 GMT
COPY multi:b3339e410120d82bf4e9d9934ea62d58e85e63f5685435dca318feb368d23c5a in /startup/ 
# Wed, 30 Mar 2022 10:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.5-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:57:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 10:57:22 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Mar 2022 10:57:23 GMT
VOLUME [/data /logs]
# Wed, 30 Mar 2022 10:57:24 GMT
EXPOSE 7473 7474 7687
# Wed, 30 Mar 2022 10:57:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 10:57:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee14fdb7a0a09a9e31998d2906081734dba985b95da3f35b7bd79d79b73330`  
		Last Modified: Tue, 29 Mar 2022 01:37:54 GMT  
		Size: 1.4 MB (1361189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad02f86dd5a08282bd579b46a15ad104740965ba6041b55cd6577546b807715`  
		Last Modified: Tue, 29 Mar 2022 01:44:05 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8f189a638f733fdf08e8ac8d579e196d88e34855d5121a93aa2247f5aa0223`  
		Last Modified: Tue, 29 Mar 2022 01:44:26 GMT  
		Size: 200.9 MB (200939335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5b36ace2abc580a9f282bab59a0baf5908050b236eed478f8117b548c5470c`  
		Last Modified: Wed, 30 Mar 2022 11:04:22 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30ac842cf93a07d01b8dc7a53beaa9fbd02e09abe62466ff85d76730f43438b`  
		Last Modified: Wed, 30 Mar 2022 11:04:22 GMT  
		Size: 7.5 KB (7538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3949cc0edcb47c9b61824fa941b5db4b1a58a161cd9e2a32e117315f991a77d3`  
		Last Modified: Wed, 30 Mar 2022 11:04:35 GMT  
		Size: 211.4 MB (211381324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
