## `openjdk:17-ea-12-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:c7952f51dfd8a9afc457671d858e91766912bcbe8a4466238be5f1c9c65ea8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-ea-12-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:cdb7ad2bbafc229d83c9f548627430e9735a2fec8d87e38570542cdd844ba30b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216452899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06802af1a3b8c99728a3f84a94c74a6e63d9c63ece33970fe77e1f6309c29710`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:10:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:10:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 09 Feb 2021 17:10:18 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Feb 2021 17:10:18 GMT
ENV LANG=C.UTF-8
# Wed, 03 Mar 2021 23:38:53 GMT
ENV JAVA_VERSION=17-ea+12
# Wed, 03 Mar 2021 23:39:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='e281f7d1fd2aaa858b02d5be451c51a9ed836c78d002cb82b114e6c36041eebf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ae713390655d0cfd8302cb2c840553404a3e366162ba5b9a2410ea7b6f1c27'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 03 Mar 2021 23:39:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91c0c19c84860aaa974864243509770a5b009f3a88b4a228010a9ade71ac968`  
		Last Modified: Tue, 09 Feb 2021 17:20:14 GMT  
		Size: 3.3 MB (3267910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828cc7cfd65faf51f4ee90844aed4b96bd2265aa26db758e2d72f5ea54ce5af6`  
		Last Modified: Wed, 03 Mar 2021 23:46:29 GMT  
		Size: 186.1 MB (186089847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
