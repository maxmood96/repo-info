## `openjdk:25-ea-29-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:298cdf7e1738c5933a72bb0a3859607f15bfa200a4bf628f783e9252fe5fcb39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-29-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:f41621fbbb6cf129a39f859e4982f61e5887f2a9ee2e0044d70331eb1cb3f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255017841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef97444d9b3fba05a9cfc433a31cdb6aefebc2b34f4e10c9cc59cac360f61a6`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 Jun 2025 00:48:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 28 Jun 2025 00:48:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_VERSION=25-ea+29
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='4fcf990db7180589d31e39c0985acb5d19a6992d77c94892636b4035b004dd3f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='565ce268822423c068fb97a832ad2c4add94427561e8e3ce29057fb8ccfbb72e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599e3dc6f37d4ef505abe4cb751b06d4f458cac2c626a486569164460fcc4f3`  
		Last Modified: Tue, 01 Jul 2025 02:32:13 GMT  
		Size: 1.6 MB (1583579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aa8b84e93a75c61192559bfe3cb8112078c9fa1976e3cb77e301cf7509ca3f`  
		Last Modified: Tue, 01 Jul 2025 06:28:20 GMT  
		Size: 223.2 MB (223178215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-29-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f6f8a5909bf897027a65311647e9011e8112b03feb60c8348c948d9032647d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cdae885090c9d1bae4e546eb5ec2a2ee7305a21b396b68f918548fdc0aabc2`

```dockerfile
```

-	Layers:
	-	`sha256:1c5d827bbf96d9ceec16cacfd483612aed1c271aa476ef812f0a05e4c59d4558`  
		Last Modified: Tue, 01 Jul 2025 06:23:43 GMT  
		Size: 2.9 MB (2942650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd906c56db7ade175ed2cfc4d777503c7d5f6001f7c130ff599fd82b3f21708`  
		Last Modified: Tue, 01 Jul 2025 06:23:44 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-29-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:11221b3e5d9cd2beca783c8de9cd8fcb1064f6119d6bfbea67a3b3075d5987c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251286961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77a021c3c94b615c61fa665039317f75a9aa60432526cca6ad34c8b81d0dc29`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 Jun 2025 00:48:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 28 Jun 2025 00:48:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_VERSION=25-ea+29
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='4fcf990db7180589d31e39c0985acb5d19a6992d77c94892636b4035b004dd3f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='565ce268822423c068fb97a832ad2c4add94427561e8e3ce29057fb8ccfbb72e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480e6ba42e9b93790207d2cffe82f71c4bbfb92871f7982c3a5ba4ce9b96e222`  
		Last Modified: Tue, 01 Jul 2025 07:35:13 GMT  
		Size: 1.6 MB (1567207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501d9135a40c91ae4d5887c8f95064ff76bc98e11f098041b9dccd26678c032c`  
		Last Modified: Tue, 01 Jul 2025 12:21:31 GMT  
		Size: 221.0 MB (220975614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-29-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:44d19dc0d9d55719405befe5f14a0f7a5b7f9cfd790e92aacdf7e7149dd18f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe89db61087121916de5ff00bdd970b8ed7ff38b7b00e3cac933ad36888bfa`

```dockerfile
```

-	Layers:
	-	`sha256:c01c25b99df253c3202b6095c17ce24bf862784d09cfad54f90bb738c067cc3f`  
		Last Modified: Tue, 01 Jul 2025 09:23:36 GMT  
		Size: 2.9 MB (2942302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6249c19b8675661f163b5bb312c2de77dfb7c0ad5df4b8189b19a696541bead`  
		Last Modified: Tue, 01 Jul 2025 09:23:37 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
