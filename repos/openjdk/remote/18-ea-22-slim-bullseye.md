## `openjdk:18-ea-22-slim-bullseye`

```console
$ docker pull openjdk@sha256:513ab1422512c33c87ab6e49f38abcd4f962cde240ee90684af3f18a314faece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-22-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:707dedb1245a645e5859bb79462c53cef7846ba447731b4d5640be0fc2b3f125
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221583947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03fc506dd2f5806ae0628d561dc7d0353d9e5df598b9e7f90286567cbd7bac9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:27:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:27:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 12 Oct 2021 16:27:47 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 16:27:47 GMT
ENV LANG=C.UTF-8
# Thu, 11 Nov 2021 02:28:35 GMT
ENV JAVA_VERSION=18-ea+22
# Thu, 11 Nov 2021 02:28:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/22/GPL/openjdk-18-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='71124796aac929f184d54cf5b2a3ba3a31c0cef1ba9b5b5e1535ec5a5d482a8b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/22/GPL/openjdk-18-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='714a0b84e6ed39e5442ca0044dab9ebecddeceffc9b78aed8e4d7ba2fbefb8aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 11 Nov 2021 02:28:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225be9814eda07dabebf0e4deb415366f34b2cfe12ef1ad167ba1104423f42d7`  
		Last Modified: Tue, 12 Oct 2021 16:42:59 GMT  
		Size: 1.6 MB (1582043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94532e4ea740fa348bd5588336eb055aa252dca675396529409e0f2e392c981`  
		Last Modified: Thu, 11 Nov 2021 02:36:33 GMT  
		Size: 188.6 MB (188644593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
