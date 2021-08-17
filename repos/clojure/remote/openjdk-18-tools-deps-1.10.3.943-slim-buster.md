## `clojure:openjdk-18-tools-deps-1.10.3.943-slim-buster`

```console
$ docker pull clojure@sha256:f4a1a39b0ba268dbc9ccbeb68e5d70757d54fdfea82341b5326da70a231c3f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps-1.10.3.943-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:99488edfee7b7e990777edb94f455ad161d61987e6926703fdc60071e42d3fe0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256679894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aa67733491abbacd4324a4916ece7fff9c3899a565f15f27e20211faa69d34`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Tue, 17 Aug 2021 06:53:11 GMT
ENV JAVA_VERSION=18-ea+10
# Tue, 17 Aug 2021 06:53:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='f02c5e52c193b349688216e85ab6fb67548861e93d96dd454f74881abfb696b2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6a6ba79485e560d0d7687152a2a1dfa92cbe80871f16eb24b52e01274f9f4f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 Aug 2021 06:53:26 GMT
CMD ["jshell"]
# Tue, 17 Aug 2021 18:39:08 GMT
ENV CLOJURE_VERSION=1.10.3.943
# Tue, 17 Aug 2021 18:39:08 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 18:39:25 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "f1fdb786fa8b9ef3a08d0b331a51861cd5a6eea277e93bbad64bf37774df17c6 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 17 Aug 2021 18:39:26 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:623fce750fc9ecbad6c143f1f03306e71fdd8829fc607299aee32bcea2d137d3`  
		Last Modified: Tue, 17 Aug 2021 07:00:15 GMT  
		Size: 187.8 MB (187845989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c51019a090ee4dde10c2f82a5d1be006fa44f73d8c252a28923aedcd6161f6`  
		Last Modified: Tue, 17 Aug 2021 18:47:15 GMT  
		Size: 38.4 MB (38419152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps-1.10.3.943-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74c0bd2961835a50c93cc837812a63b8f37c88d1101f9d5e30ec218e301ad737
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253543859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa963968daf404257f446e7a8cdad2012b3a15b43125c3b6f1c41ea6ff8e7c`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Tue, 17 Aug 2021 06:04:06 GMT
ENV JAVA_VERSION=18-ea+10
# Tue, 17 Aug 2021 06:04:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='f02c5e52c193b349688216e85ab6fb67548861e93d96dd454f74881abfb696b2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6a6ba79485e560d0d7687152a2a1dfa92cbe80871f16eb24b52e01274f9f4f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 Aug 2021 06:04:19 GMT
CMD ["jshell"]
# Tue, 17 Aug 2021 15:15:37 GMT
ENV CLOJURE_VERSION=1.10.3.943
# Tue, 17 Aug 2021 15:15:37 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 15:15:58 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "f1fdb786fa8b9ef3a08d0b331a51861cd5a6eea277e93bbad64bf37774df17c6 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 17 Aug 2021 15:15:58 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:5319062f85e69f8cb29cc6342d5d5de703b4aaf14b9cac91bc0003aa7a14cf36`  
		Last Modified: Tue, 17 Aug 2021 06:15:58 GMT  
		Size: 186.6 MB (186596948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31c682638f4ac723b724d3ba8b4d8df5f6380a5d28032a997303091256b3a7`  
		Last Modified: Tue, 17 Aug 2021 15:24:53 GMT  
		Size: 37.9 MB (37912978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
