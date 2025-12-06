## `openjdk:27-ea-trixie`

```console
$ docker pull openjdk@sha256:c7ac1505ebff97bf3396e12fd5cb2e4f80e6bf6e3b909eb71a81a657c90a9d7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:9bc389614641d34788e6f1599165dbf7aea0d86109b42170f5380fa6f8a67d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386750853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff8af66fe2cdc74d278e0c50e51a8a0ca9683fe649dd08fc025724ab6ae34bf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 06 Dec 2025 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 06 Dec 2025 00:35:55 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:55 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:55 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:35:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cc7a5412a72b1fb6d7bb4afaeecd2854f0994592a46187e0fb9e9045d203d5`  
		Last Modified: Sat, 06 Dec 2025 00:36:34 GMT  
		Size: 16.1 MB (16061683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095c601286b1f2ffa90704c9d7da45161d68997d89ffc014ca902465b773352c`  
		Last Modified: Sat, 06 Dec 2025 00:38:34 GMT  
		Size: 228.0 MB (228006711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:bab701c04411c3223a3a805adbb8a93ab8385dfff15348a67ffe276b27e7f835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb27a4b9017c77ca61182fb10074b70a4ab10f130987071193971846e6dbdb1`

```dockerfile
```

-	Layers:
	-	`sha256:c66c60c49f9f034dfec7e9f691c04d254622e89587bbac41427f1338ea0822db`  
		Last Modified: Sat, 06 Dec 2025 01:27:00 GMT  
		Size: 8.5 MB (8509931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e190a200de8af92545c408e16e1d7b66f8b3318c97f42e2db63d89b9b63d708`  
		Last Modified: Sat, 06 Dec 2025 01:27:01 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bcfd35f759c855e3cfcffccad2053d37c872f9f9cc7655bd6b96673d7efb748a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384244347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e32de2ffbc4b2935077ca5f1c48c8aa8e7759bf86ba57da20b92795ae59b8e5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 06 Dec 2025 00:35:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 06 Dec 2025 00:35:55 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:55 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:55 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:35:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fe09cc62f1287a7fae7eacf3d58c6486a1e7e3a0abc278ae806eb4d7cc5aec`  
		Last Modified: Sat, 06 Dec 2025 00:36:37 GMT  
		Size: 16.1 MB (16070852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f4392a0544524525da44d14da9607b6d5aa4c17145518af213c356b1d2027`  
		Last Modified: Sat, 06 Dec 2025 00:36:40 GMT  
		Size: 225.9 MB (225917490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0699c2c200afe362fa2ed8802a5f959014c7a77b0fd9d1c93a225346b17b93e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cd7836b98708a3bbfeab1b4b269b7fd994490fdb15ebba6e17c72207d4795`

```dockerfile
```

-	Layers:
	-	`sha256:76859b07839995d2c18d813840de235a1cb039dc5b5e11e498ff7f13690b6092`  
		Last Modified: Sat, 06 Dec 2025 01:27:08 GMT  
		Size: 8.7 MB (8704721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecf4f27222b1424ee5a957a3e70b98b9525fb97d1f9668241f1f0bdc8e653828`  
		Last Modified: Sat, 06 Dec 2025 01:27:08 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
