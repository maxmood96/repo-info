## `openjdk:21-slim-buster`

```console
$ docker pull openjdk@sha256:d03d11624b9a793d872c6176929dc7347ffdade2503848da25141c31384418fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:87719f24685af956745e0ea2d20ace6daaf73e62213562144ee1388da7652e50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229772221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041b6d265d07f2b92a68bc65fd5556101569fe8263a8b21b90e7c3fc9cb96b5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:11:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 21 Dec 2022 12:11:23 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 12:11:24 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:11:24 GMT
ENV JAVA_VERSION=21-ea+2
# Wed, 21 Dec 2022 12:11:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/2/GPL/openjdk-21-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='8070902e5bfbb71a4e7c723bb0439faeb9f3127e1fb048f7ed4e6a5abc5a3505'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/2/GPL/openjdk-21-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='011358a514a8d4030c36bbd5b7d7fb5c404f326498f4c832ee5f890fff8709db'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 21 Dec 2022 12:11:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3bbd683992a77729adf4c48b2abf5433b10ca0efd1763143381041d3b912d6`  
		Last Modified: Wed, 21 Dec 2022 12:18:58 GMT  
		Size: 3.3 MB (3275903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c245056e41394404da1cd7d42d6195e64fbf78642a8a407019741ea67785e7`  
		Last Modified: Wed, 21 Dec 2022 12:19:12 GMT  
		Size: 199.4 MB (199355987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d8ed6d33e921978c01210677aad1d302f19fad365f6fa1f1c1c3a8a3f801f95b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226906153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c6386cd389666bed66a625f81886a474119bf6878202c388d1bf364d5025d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:54:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:54:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 21 Dec 2022 03:54:16 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 03:54:16 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 03:54:17 GMT
ENV JAVA_VERSION=21-ea+2
# Wed, 21 Dec 2022 03:54:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/2/GPL/openjdk-21-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='8070902e5bfbb71a4e7c723bb0439faeb9f3127e1fb048f7ed4e6a5abc5a3505'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/2/GPL/openjdk-21-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='011358a514a8d4030c36bbd5b7d7fb5c404f326498f4c832ee5f890fff8709db'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 21 Dec 2022 03:54:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ce4a2d8593279f5ee148800b1072137f52a82ed3f7fc56ca4b7d8f85c0883e`  
		Last Modified: Wed, 21 Dec 2022 04:01:14 GMT  
		Size: 3.1 MB (3129404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd41867c5efae0224b46f6a79d18d8e7d52db07eb8698e3151a6ca944a65056`  
		Last Modified: Wed, 21 Dec 2022 04:01:26 GMT  
		Size: 197.9 MB (197861843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
