## `openjdk:17-ea-16-slim`

```console
$ docker pull openjdk@sha256:482792d895b197ece5f92fbb198b4dde9f491e7a622e81c698db0901b0ea1793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-16-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:bb976c13dd9c40c569aa160c9f4c6c633224064ab7df2304d40a9827e00d3709
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216494148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5774ffe0d399223882c4d71578b7965cefbe7810df19c42d5059c532283c379`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:41:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 31 Mar 2021 05:41:07 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Mar 2021 05:41:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Apr 2021 18:26:26 GMT
ENV JAVA_VERSION=17-ea+16
# Fri, 02 Apr 2021 18:26:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='ee7a5b391e275d159e623b7a35008d180c0ff362e93216395412aae871a1790a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='7554740bd86ea06cfdead0b768cd15758ea76d21ba2140b9b7b9bb1e45fd0c39'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 02 Apr 2021 18:26:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875a154571f097680e56e5acc7383853036fac0e52855a4dd4fa740bfabf3f95`  
		Last Modified: Wed, 31 Mar 2021 05:52:39 GMT  
		Size: 3.3 MB (3268916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9aed0479c2a558be624d8234821bad61eddda4c0d2472d1fdade77c84e6af`  
		Last Modified: Fri, 02 Apr 2021 18:33:36 GMT  
		Size: 186.1 MB (186085939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-16-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4d18bab85e173c62b5e188923557966eda0828081dc67f457a7fe715b2474169
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211171378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81734a8a0eee57b6da99f0df6953c4eb2ef025773a68455836267ca594d6e06b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:39:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:39:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 31 Mar 2021 01:39:30 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Mar 2021 01:39:32 GMT
ENV LANG=C.UTF-8
# Fri, 02 Apr 2021 19:14:43 GMT
ENV JAVA_VERSION=17-ea+16
# Fri, 02 Apr 2021 19:15:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='ee7a5b391e275d159e623b7a35008d180c0ff362e93216395412aae871a1790a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='7554740bd86ea06cfdead0b768cd15758ea76d21ba2140b9b7b9bb1e45fd0c39'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 02 Apr 2021 19:15:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fde6667c188c81fcddee021ccbb3e054ebe83350fd4609e17a3d37f0ec7f9d`  
		Last Modified: Wed, 31 Mar 2021 01:49:41 GMT  
		Size: 3.1 MB (3118896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7748c9dc7e98549082dafb2519d3d4b9444d80703e528b41a73d31e063df0bc`  
		Last Modified: Fri, 02 Apr 2021 19:23:26 GMT  
		Size: 182.1 MB (182147969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
