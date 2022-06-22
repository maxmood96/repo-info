## `openjdk:19-ea-27-jdk-slim`

```console
$ docker pull openjdk@sha256:eed9c7743e42d8b221a248d2690e1ce0a316fa2ee89694c2f581d703cd31be79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-27-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:1542b6a379c8ec590764d201f6e0ab7b1d321cada9aefa7a0b12904da2c7dbd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229470788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf45af98fdd2279fbad08e281426a1b425c3aaefdd5494177f6a85490d523be8`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:16:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Sat, 28 May 2022 02:16:35 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:16:35 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 01:22:32 GMT
ENV JAVA_VERSION=19-ea+27
# Wed, 22 Jun 2022 01:22:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/27/GPL/openjdk-19-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='d88a9e824ce2c65fd634463856a6af2e8aad09a3b005a6ae9f3529b972d184c4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/27/GPL/openjdk-19-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7e93f0cde43b50161e5817e8a12907f5a2e74dbd63a4fa99d059ba4afdab02ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 22 Jun 2022 01:22:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4201f96d0f3d4b724b280e8a3ea741805b8fffd20424803de8f49f392cf57002`  
		Last Modified: Wed, 22 Jun 2022 01:35:31 GMT  
		Size: 196.5 MB (196509222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
