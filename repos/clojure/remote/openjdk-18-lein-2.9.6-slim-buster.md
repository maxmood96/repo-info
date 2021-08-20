## `clojure:openjdk-18-lein-2.9.6-slim-buster`

```console
$ docker pull clojure@sha256:9bf2af43ca5684799967c5692638259cfccca9ba35b96a9bdae04239d2edae70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-lein-2.9.6-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:e25e458d766a95a02d70e09fc37e40b8701fc688e3d78046e3d6a58ebd617315
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234288906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2410114eb00e51cbc28c4cd6d6182731162c70eff64582c3670e7723b9bf6e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:53:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 17 Aug 2021 06:53:11 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:53:11 GMT
ENV LANG=C.UTF-8
# Thu, 19 Aug 2021 22:29:20 GMT
ENV JAVA_VERSION=18-ea+11
# Thu, 19 Aug 2021 22:29:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='593243ad4eb9339cec9d7675ff01fb4d7b816c1b1f68d4e54d0dc4f99d8f55f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8efa12ef6e1acab1a4cc5dba5a45dcb828fa0265e409cd0cf2e8e9eec4ad8f0f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 Aug 2021 22:29:35 GMT
CMD ["jshell"]
# Thu, 19 Aug 2021 23:08:40 GMT
ENV LEIN_VERSION=2.9.6
# Thu, 19 Aug 2021 23:08:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 19 Aug 2021 23:08:40 GMT
WORKDIR /tmp
# Thu, 19 Aug 2021 23:08:52 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 19 Aug 2021 23:08:52 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 19 Aug 2021 23:08:52 GMT
ENV LEIN_ROOT=1
# Thu, 19 Aug 2021 23:08:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 19 Aug 2021 23:08:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427b7134c0c7b2e1d9cc703e20a84b850cbbf34ef654cfa0db710678a99da78b`  
		Last Modified: Tue, 17 Aug 2021 07:00:00 GMT  
		Size: 3.3 MB (3268768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e628b12479503916e24674a2a918dadb02e86ffbe093a0e7382ad9d1afb7c2c`  
		Last Modified: Thu, 19 Aug 2021 22:36:04 GMT  
		Size: 187.9 MB (187867380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0409e1e62ac415cf50c18ea4e33d77ec127b4041a4ff232638cef577f1a812c0`  
		Last Modified: Thu, 19 Aug 2021 23:13:49 GMT  
		Size: 11.8 MB (11803051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c551a7d5146b92f0ee31d88b453b72c0abea5480b346d0d4e760213c717442ce`  
		Last Modified: Thu, 19 Aug 2021 23:13:49 GMT  
		Size: 4.2 MB (4203722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-lein-2.9.6-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4a350858f27c8ed64070aa9d7564c7206d91641d181f21d50e00bd050028e0dc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231644175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dce16c325f35c0e255c5bd474f2c97e34223cd51faa1c82e79152b07b0304a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:04:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:04:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 17 Aug 2021 06:04:06 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:04:06 GMT
ENV LANG=C.UTF-8
# Thu, 19 Aug 2021 20:41:51 GMT
ENV JAVA_VERSION=18-ea+11
# Thu, 19 Aug 2021 20:42:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='593243ad4eb9339cec9d7675ff01fb4d7b816c1b1f68d4e54d0dc4f99d8f55f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8efa12ef6e1acab1a4cc5dba5a45dcb828fa0265e409cd0cf2e8e9eec4ad8f0f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 Aug 2021 20:42:10 GMT
CMD ["jshell"]
# Thu, 19 Aug 2021 22:34:10 GMT
ENV LEIN_VERSION=2.9.6
# Thu, 19 Aug 2021 22:34:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 19 Aug 2021 22:34:11 GMT
WORKDIR /tmp
# Thu, 19 Aug 2021 22:34:22 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 19 Aug 2021 22:34:22 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 19 Aug 2021 22:34:22 GMT
ENV LEIN_ROOT=1
# Thu, 19 Aug 2021 22:34:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 19 Aug 2021 22:34:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82a27af984eefbe6b82ccb775aead56e92f82cf16d079218087ebe132125cf5`  
		Last Modified: Tue, 17 Aug 2021 06:15:41 GMT  
		Size: 3.1 MB (3118861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937780d44fe5eb665a71c71605ccd575fca3517f672bab075e89f18fe34cf797`  
		Last Modified: Thu, 19 Aug 2021 20:53:52 GMT  
		Size: 186.6 MB (186603707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab796cbdec31c73364c186de6a2abacac2968b75c57ded3dd4917e6be42c1d26`  
		Last Modified: Thu, 19 Aug 2021 22:41:16 GMT  
		Size: 11.8 MB (11802859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f842ae7a5bb2e85e8510421733fa0ad1556ddb1bfe18e8f17ade21ee7293ae`  
		Last Modified: Thu, 19 Aug 2021 22:41:16 GMT  
		Size: 4.2 MB (4203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
