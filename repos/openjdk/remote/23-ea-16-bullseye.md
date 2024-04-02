## `openjdk:23-ea-16-bullseye`

```console
$ docker pull openjdk@sha256:b3364239f61ddbbf9a3c57043ef7f8eeb18e7e9e21599bee0b642216e60be08f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-16-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:80d50e4b81d71fc357892a7973e5f4d7b59d9f99207695b6dc5dd28c5878ba76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350455334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec0f44517545c8f608b3ae90c79fcd33e8e15fe0f609e7abd84abceb7191250`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 29 Mar 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+16
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='9a5d2039ec965c15d80dbc5106c9e2f1c4a80975e18d308b55f0a3d892f24358'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d654c940f0c5b9ed7549f29066599b2caedbaf2ec45f3745ac35e265c288e2d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847182d45c0f6048300303c3d8f0879bbc63161247eb68ac4eb0f8827fdf9b9`  
		Last Modified: Mon, 01 Apr 2024 23:50:19 GMT  
		Size: 14.1 MB (14071333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ae3ca49211ae7ad0d433fedb1b76d9d2e729c753e13e8fb533e304d349e4c8`  
		Last Modified: Mon, 01 Apr 2024 23:50:23 GMT  
		Size: 210.9 MB (210947069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-16-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:67fe034549adb644cd631af66346bf5b6a8954f1ba97effba4651309df02eec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a742c85287a457c7f134378880308a81459f11b45d2a206c68788554c41c58b3`

```dockerfile
```

-	Layers:
	-	`sha256:dbd87686ac88af670287ea109c2ece1e037326c72b98b31e8964847b8d2bf1b2`  
		Last Modified: Mon, 01 Apr 2024 23:50:19 GMT  
		Size: 8.2 MB (8157041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5833123b58395efee2b2faa094183e2189599bc59ae9642ba29a3c52ce4ea0bf`  
		Last Modified: Mon, 01 Apr 2024 23:50:18 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json
