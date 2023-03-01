## `openjdk:21-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:92991ff05279c599ccb2a40eddab21e141359a82ecd2a397dcbac982490ae7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:9e43f2a8b22ffa19887863eaec4874adf7b68642d6d58e67e4184fc6c29f341a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232731289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e09b3667d52205459edc387ec4f6b2942e314537ff7c5e082463e10aa4a1ab1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:47:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 09 Feb 2023 10:47:20 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 10:47:20 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2023 01:30:43 GMT
ENV JAVA_VERSION=21-ea+11
# Tue, 28 Feb 2023 01:30:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='44d5639ae3005e8f6a494ab42506f7fbbe7c366a17c7da792bcaf21a04f5be13'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4f1bfbab4042464ed8c0b6e462354db5e97320b7c74d257639fc4c05d3ce4827'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Feb 2023 01:30:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10286f48c71be2a630e155ceb33e8e5132e861088b8d5db5ae0b2589912a958d`  
		Last Modified: Thu, 09 Feb 2023 10:54:07 GMT  
		Size: 1.6 MB (1582324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ba47bce23a410edb5071da9251945ce3fa8d48a4f64570080a5a522b0aadb8`  
		Last Modified: Tue, 28 Feb 2023 01:35:01 GMT  
		Size: 199.7 MB (199737155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8eeb082c80f465654f92b5359691c08a43fe0df9b2938b518ce13a8d1c544261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229859066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c6d89363982a8a58c47d0b50e0813dae4758c1942cfd6a713edbdab6d7b406`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:24:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 05:24:25 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:24:25 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 05:24:25 GMT
ENV JAVA_VERSION=21-ea+11
# Wed, 01 Mar 2023 05:24:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='44d5639ae3005e8f6a494ab42506f7fbbe7c366a17c7da792bcaf21a04f5be13'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4f1bfbab4042464ed8c0b6e462354db5e97320b7c74d257639fc4c05d3ce4827'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Mar 2023 05:24:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dd3b27db5b90473cd40b6a58bd74aaa2fa2f05afe0691341705918804f631d`  
		Last Modified: Wed, 01 Mar 2023 05:28:30 GMT  
		Size: 1.6 MB (1566316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8ff17c40fd1da433be132c6ef6ffb57d3e7bcc16135c7af3debad6076f4f31`  
		Last Modified: Wed, 01 Mar 2023 05:28:41 GMT  
		Size: 198.2 MB (198229936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
