## `openjdk:22-ea-5-slim-bookworm`

```console
$ docker pull openjdk@sha256:76e2932b0f9759e050d5558674879803483e8409dc1954da9806f827f682bbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:22-ea-5-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:88791e68e0d1930cd6249877413d671448b41473b7cbff923587d00af0635ec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238179819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e55ba0a0b477539f0b60be57443252363e242d43ebfc495f3fa2f06b1df2207`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:58 GMT
ADD file:bd80a4461150784e5f2f5a1faa720cc347ad3e30ee0969adbfad574c316f5aef in / 
# Tue, 04 Jul 2023 01:19:58 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 01:52:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 04 Jul 2023 01:52:41 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 01:52:41 GMT
ENV LANG=C.UTF-8
# Mon, 10 Jul 2023 20:47:21 GMT
ENV JAVA_VERSION=22-ea+5
# Mon, 10 Jul 2023 20:47:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/5/GPL/openjdk-22-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='64f27322499a7876328a444330c8a1c5ff621b3db22129d046b7e8c2e8451e3a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/5/GPL/openjdk-22-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='4a0df847d4239efb0ea7c9a05fcfcc0f2205acfeb6628f9df38f4775d7ad9fd1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 10 Jul 2023 20:47:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:faef57eae888cbe4a5613eca6741b5e48d768b83f6088858aee9a5a2834f8151`  
		Last Modified: Tue, 04 Jul 2023 01:25:03 GMT  
		Size: 29.1 MB (29124829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbdb27ec859f702c52e07508d08c6644cdff01fc5028ae06b5440b5e48d2937`  
		Last Modified: Tue, 04 Jul 2023 01:57:48 GMT  
		Size: 4.0 MB (4008037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fda07a29b0d73daf71aa8e7634cb67eaf232de8ed29b5ba157ce0da15e316f`  
		Last Modified: Mon, 10 Jul 2023 20:52:50 GMT  
		Size: 205.0 MB (205046953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
