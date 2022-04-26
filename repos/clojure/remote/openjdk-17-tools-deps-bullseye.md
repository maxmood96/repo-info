## `clojure:openjdk-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:2c0045c1dfa1f3ce3038a5cb03cab9afa9807922f4ca1ad517ca5417b52ef39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:44391e91bfe310cfac363b73cf7c16e135c20613ae04cf11e996487228f19dc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350485291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00df58d2bb11d1f3a861de5e83209e5b052317983feb41bd9c26ccb82513d20c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:15 GMT
ADD file:3a81c181c66f226bd6abd48d0c7ed8a9c599c9f521ec7229286c83161afec8c2 in / 
# Wed, 20 Apr 2022 04:43:16 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:57:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:57:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 06:58:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:47:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:50:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 20 Apr 2022 10:50:50 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:50:50 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:50:50 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 20 Apr 2022 10:51:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Apr 2022 10:51:02 GMT
CMD ["jshell"]
# Tue, 26 Apr 2022 00:37:22 GMT
ENV CLOJURE_VERSION=1.11.1.1113
# Tue, 26 Apr 2022 00:37:22 GMT
WORKDIR /tmp
# Tue, 26 Apr 2022 00:37:30 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7677bb1179ebb15ebf954a87bd1078f1c547673d946dadafd23ece8cd61f5a9f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 26 Apr 2022 00:37:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 26 Apr 2022 00:37:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 26 Apr 2022 00:37:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Apr 2022 00:37:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6aefca2dc61dcbcd268b8a9861e552f9cdb69e57242faec64ac120d2355a9c1a`  
		Last Modified: Wed, 20 Apr 2022 04:47:57 GMT  
		Size: 54.9 MB (54941777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967757d5652770cfa81b6cc7577d65e06d336173da116d1fb5b2d349d5d44127`  
		Last Modified: Wed, 20 Apr 2022 07:05:43 GMT  
		Size: 5.2 MB (5155716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c357e2c68cb3bf1e98dcb3eb6ceb16837253db71535921d6993c594588bffe04`  
		Last Modified: Wed, 20 Apr 2022 07:05:45 GMT  
		Size: 10.9 MB (10874928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c766e27afb21eddf9ab3e4349700ebe697c32a4c6ada6af4f08282277a291a28`  
		Last Modified: Wed, 20 Apr 2022 07:06:05 GMT  
		Size: 54.6 MB (54578663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e454664a629c8e4cac99685ba1b624982040c45466f197f649234a8e132803`  
		Last Modified: Wed, 20 Apr 2022 11:00:48 GMT  
		Size: 14.1 MB (14071513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303943476b6f5143642c36b70f95ce88a30634496fdbf41b8f5c5deaf16b48f7`  
		Last Modified: Wed, 20 Apr 2022 11:05:54 GMT  
		Size: 187.6 MB (187628474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc989978d82ac0fbaa1fc4527ee69f57aeb300400cb503f4d8e8928df3246afa`  
		Last Modified: Tue, 26 Apr 2022 00:47:13 GMT  
		Size: 23.2 MB (23233190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffde408c8ad887bbfc68787f781dc8f4afba964cd4723eccadd2fd8ca8e656d`  
		Last Modified: Tue, 26 Apr 2022 00:47:11 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb5260d74d43a5518a7bb82ed3651b81cac582a4bef707d11c55644286c42b`  
		Last Modified: Tue, 26 Apr 2022 00:47:12 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94d4ce14b9955cf1b97579381721cd9c91d495c25ee6b646863792aa607d890a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348895590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4318983efaa04f2d969449acb681ea56203572d1699f4870e3b12879331dad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Apr 2022 04:28:55 GMT
ADD file:ece192802cbdaf1a141d04f0c2e90cfd3479e5e3e82c6a00206970684494cf48 in / 
# Wed, 20 Apr 2022 04:28:56 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:44:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:44:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 06:44:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:24:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:28:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 20 Apr 2022 10:28:21 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:28:23 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 20 Apr 2022 10:28:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Apr 2022 10:28:40 GMT
CMD ["jshell"]
# Tue, 26 Apr 2022 00:55:44 GMT
ENV CLOJURE_VERSION=1.11.1.1113
# Tue, 26 Apr 2022 00:55:45 GMT
WORKDIR /tmp
# Tue, 26 Apr 2022 00:55:54 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7677bb1179ebb15ebf954a87bd1078f1c547673d946dadafd23ece8cd61f5a9f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 26 Apr 2022 00:55:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 26 Apr 2022 00:55:56 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 26 Apr 2022 00:55:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Apr 2022 00:55:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:83d5dcfea08e6927083bc886bf182fc39d87bb04b54b63002ac0c4c0b9aab682`  
		Last Modified: Wed, 20 Apr 2022 04:35:19 GMT  
		Size: 53.6 MB (53633096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cfa86b7b1aca6d694057e4d42ee1440527f41c00b9e577df729244380c9eba`  
		Last Modified: Wed, 20 Apr 2022 06:54:10 GMT  
		Size: 4.9 MB (4938663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c79b19335f27cc78840bf9159e875322f3252ac06113c73756f9d4fba905f9b`  
		Last Modified: Wed, 20 Apr 2022 06:54:10 GMT  
		Size: 10.7 MB (10656971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ecaf08eac09037b05465ab97a1b8f7bc9b7a9b1fcef900dedd7dba9bbcf4d`  
		Last Modified: Wed, 20 Apr 2022 06:54:32 GMT  
		Size: 54.7 MB (54672934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b174d41b9ea1124e2245788f2c290f940eca707dcc0446cd302b01aaeb5c82`  
		Last Modified: Wed, 20 Apr 2022 10:45:28 GMT  
		Size: 15.5 MB (15525740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcad0d6cbc9566a9060cce10d4afebc73de9f59e90ed2ba2e9fe4e6767013600`  
		Last Modified: Wed, 20 Apr 2022 10:51:07 GMT  
		Size: 186.5 MB (186472881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c95c24d26e516d1e49bd5d1d829bac56918c49686db109c96f4be3417a6140`  
		Last Modified: Tue, 26 Apr 2022 01:10:21 GMT  
		Size: 23.0 MB (22994277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d115092f9a33b228aea90d803c9390c82d90627e4af45f869ca1a9dfd45f1a`  
		Last Modified: Tue, 26 Apr 2022 01:10:19 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bde589d3008e48385ef8ad5bec2c3859b8e020e2e7b96f165a1379ca649e3b`  
		Last Modified: Tue, 26 Apr 2022 01:10:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
