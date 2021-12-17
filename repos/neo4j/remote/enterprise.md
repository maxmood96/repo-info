## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:5b026348c6ebb42b883b4d64dd4d0c3fe60fe102e2f5d349796d077d8b16b9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:08d850004e916d9384417dc213779bb02079eb9f9b53d6d7b7945ab998318017
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.8 MB (444791811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bef759bc64f148fb166e070cee02e71c67f9385ede93922f56f25d56f1e054`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:58 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:58 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:59 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:59 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:35:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:35:38 GMT
CMD ["jshell"]
# Tue, 14 Dec 2021 21:20:50 GMT
ENV NEO4J_SHA256=e524ccb258274645bb684c9f09162bc5e18768d58680dd0fe09afe9d11b63817 NEO4J_TARBALL=neo4j-enterprise-4.4.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 14 Dec 2021 21:20:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.1-unix.tar.gz
# Tue, 14 Dec 2021 21:20:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 14 Dec 2021 21:20:52 GMT
COPY multi:220c2663e29181f5cd4d1cc8ff4ea55bca5bd66e60ecec0890d11b2c206bdb54 in /tmp/ 
# Tue, 14 Dec 2021 21:21:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.1-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && set -eux; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64')             tinisha="12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855";             tiniurl="https://github.com/krallin/tini/releases/download/v0.18.0/tini"; 			;; 		'arm64')             tinisha="7c5463f55393985ee22357d976758aaaecd08defb3c5294d353732018169b019";             tiniurl="https://github.com/krallin/tini/releases/download/v0.18.0/tini-arm64"; 			;; 		*) echo >&2 "Neo4j does not currently have a docker image for architecture $dpkgArch"; exit 1 ;; 	esac     && curl -L --fail --silent --show-error ${tiniurl} > /sbin/tini     && echo "${tinisha}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && apt-get -y purge --auto-remove curl     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Dec 2021 21:21:11 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Dec 2021 21:21:11 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 Dec 2021 21:21:11 GMT
VOLUME [/data /logs]
# Tue, 14 Dec 2021 21:21:11 GMT
COPY file:ab7ae7f90c4a2b48d55ce46bb4b2dcdc336a04742bc26d5311b62b6d1e2ce171 in /docker-entrypoint.sh 
# Tue, 14 Dec 2021 21:21:11 GMT
EXPOSE 7473 7474 7687
# Tue, 14 Dec 2021 21:21:12 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Tue, 14 Dec 2021 21:21:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f5b9b70c2f137dc70e816256e7a568a084d066e7c34c028d30a6a45438685`  
		Last Modified: Thu, 02 Dec 2021 11:47:20 GMT  
		Size: 1.6 MB (1582045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487fc3d77b36e6ef6949adfd74769b0d393dec1d06fa2657f03911fcba2b0323`  
		Last Modified: Thu, 02 Dec 2021 11:55:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c014467dc653d97b26e3de00786518336609811ef354ef313e790741abc0522a`  
		Last Modified: Thu, 02 Dec 2021 11:55:44 GMT  
		Size: 203.4 MB (203392008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be06c005dcae6e72fb2900eba03f3e9b55f039346743aeb1a7d8699ab7dce603`  
		Last Modified: Tue, 14 Dec 2021 21:28:27 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c8de3028c4bb69ecfcdab07f64d5bb310ab78968d271abcd7fd52b25771cab`  
		Last Modified: Tue, 14 Dec 2021 21:28:26 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b563e4daafd1a0c1ca6b8260e4b8fe7956abc1d36da3d4d9752d4a3ce5ed46`  
		Last Modified: Tue, 14 Dec 2021 21:28:36 GMT  
		Size: 208.4 MB (208436305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed2de7d206c565de80a79310e5241cf49ff4837027a941996533feb4ef54b3`  
		Last Modified: Tue, 14 Dec 2021 21:28:26 GMT  
		Size: 6.6 KB (6553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4776a3c2a97dff9b2f2042e9e1b9ae91e8a3b77a23b7f2b1fc35d14d40149589
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.3 MB (440333061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcabb6caf2823af4beb8989875591925861df14d009cecdfb1e9059c1a5c504d`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:08:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:08:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:08:01 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:08:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:08:03 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:08:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:08:34 GMT
CMD ["jshell"]
# Fri, 17 Dec 2021 19:08:19 GMT
ENV NEO4J_SHA256=3e4a10d8a6115a37f9c8f7c96c83c50450fd73790089945b2dd9c25436c2799f NEO4J_TARBALL=neo4j-enterprise-4.4.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Dec 2021 19:08:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.2-unix.tar.gz
# Fri, 17 Dec 2021 19:08:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 17 Dec 2021 19:08:23 GMT
COPY multi:220c2663e29181f5cd4d1cc8ff4ea55bca5bd66e60ecec0890d11b2c206bdb54 in /tmp/ 
# Fri, 17 Dec 2021 19:08:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.2-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && set -eux; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64')             tinisha="12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855";             tiniurl="https://github.com/krallin/tini/releases/download/v0.18.0/tini"; 			;; 		'arm64')             tinisha="7c5463f55393985ee22357d976758aaaecd08defb3c5294d353732018169b019";             tiniurl="https://github.com/krallin/tini/releases/download/v0.18.0/tini-arm64"; 			;; 		*) echo >&2 "Neo4j does not currently have a docker image for architecture $dpkgArch"; exit 1 ;; 	esac     && curl -L --fail --silent --show-error ${tiniurl} > /sbin/tini     && echo "${tinisha}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && apt-get -y purge --auto-remove curl     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:08:42 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Dec 2021 19:08:43 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Dec 2021 19:08:44 GMT
VOLUME [/data /logs]
# Fri, 17 Dec 2021 19:08:46 GMT
COPY file:ab7ae7f90c4a2b48d55ce46bb4b2dcdc336a04742bc26d5311b62b6d1e2ce171 in /docker-entrypoint.sh 
# Fri, 17 Dec 2021 19:08:46 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Dec 2021 19:08:47 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Fri, 17 Dec 2021 19:08:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595058421fcb005f80f2faa2434369885cb20645caed265e7b4912808701d893`  
		Last Modified: Thu, 02 Dec 2021 11:23:15 GMT  
		Size: 1.4 MB (1361242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847c13000ac6e7eb05246ab778901565fb6666b6250d9e32b84ce2fa07be4b85`  
		Last Modified: Thu, 02 Dec 2021 11:31:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562b61f5cdbc47122511903e363e95f1132c07dc74e4d519178b3fe06bb5a085`  
		Last Modified: Thu, 02 Dec 2021 11:32:06 GMT  
		Size: 200.8 MB (200768687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0de36d6985b1471301ab118b7c66fef6d8fcc66a8071d8211efef17d5f13b75`  
		Last Modified: Fri, 17 Dec 2021 19:10:11 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c7147c6f4f10547449bb88d9ab4fb6cf078b0d74d3803446ce002b4671ec59`  
		Last Modified: Fri, 17 Dec 2021 19:10:11 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053ff7956bcbf553e32e6ba467636d8c9fb2f4a5c176ec379a44f29b448197d9`  
		Last Modified: Fri, 17 Dec 2021 19:10:24 GMT  
		Size: 208.1 MB (208135388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e408e26569ff1ff4b100ff2bfbe1c23bff000f2c7a7f8cf0f831b49648615b`  
		Last Modified: Fri, 17 Dec 2021 19:10:11 GMT  
		Size: 6.6 KB (6553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
