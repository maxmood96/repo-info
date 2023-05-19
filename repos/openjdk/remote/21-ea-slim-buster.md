## `openjdk:21-ea-slim-buster`

```console
$ docker pull openjdk@sha256:577dce7cd98d975515d911f49ba34518591af20b74f00f7ad9e1c4e0e8574dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:2330d7eb0b7a85691e42d4dac9f4002b522bc16b4d0a70392eb16fe8a9e0dca6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233702717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39ec6e2c7b057d956fa6f4869e65ea4893b49d3876146875a00fd741dff500c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:20:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 03 May 2023 18:20:16 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:20:16 GMT
ENV LANG=C.UTF-8
# Fri, 19 May 2023 17:25:03 GMT
ENV JAVA_VERSION=21-ea+23
# Fri, 19 May 2023 17:25:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f3644497f76a889a341866ea29e2b3ce1c82772b1a0a827388d36cf2fd180263'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='3241d3b6b20a9520ee937d7aab42daa55e86cc251ca77f0643e4425ccf7b1348'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 May 2023 17:25:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5572f0fb7b53dfd62a51ebc6aea399bb961104546222935c7fc356213a2108`  
		Last Modified: Wed, 03 May 2023 18:22:41 GMT  
		Size: 3.3 MB (3278806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838dd14a4f34a21858bf9f36972405b339fed713559c0ae11b83786383325776`  
		Last Modified: Fri, 19 May 2023 17:29:01 GMT  
		Size: 203.3 MB (203284952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c6fb82bf08018dd8d7dc8f0e0e86e82766c312afcd4ac29b8c689d453bff0d32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230684725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6fe1a82b2f313671565e9a1b2e070abc3aca98f59aae827ae69748614cbf5d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 May 2023 00:23:05 GMT
ADD file:1d8cf95f550bb4b86ad82b22e7195179335fa3b327fd1f1ba1e6c8357ee15c94 in / 
# Wed, 03 May 2023 00:23:05 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:05:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:05:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 03 May 2023 17:05:27 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:05:27 GMT
ENV LANG=C.UTF-8
# Fri, 19 May 2023 17:49:35 GMT
ENV JAVA_VERSION=21-ea+23
# Fri, 19 May 2023 17:49:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f3644497f76a889a341866ea29e2b3ce1c82772b1a0a827388d36cf2fd180263'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='3241d3b6b20a9520ee937d7aab42daa55e86cc251ca77f0643e4425ccf7b1348'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 May 2023 17:49:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5627aec4010af613408c2ee78d5d32b9ecac22cb396d702906fb1160721f0011`  
		Last Modified: Wed, 03 May 2023 00:26:29 GMT  
		Size: 25.9 MB (25922039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9563e8b04d7a9913e093d138a52956da4d7e040127df5ba21381fc762e84eab`  
		Last Modified: Wed, 03 May 2023 17:07:53 GMT  
		Size: 3.1 MB (3131737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1087cca0c8cb1364d8574a76299954c92763927d5e1f5c824f9bb028cca28d3`  
		Last Modified: Fri, 19 May 2023 17:53:12 GMT  
		Size: 201.6 MB (201630949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
