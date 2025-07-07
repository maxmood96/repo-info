## `openjdk:25-slim-bullseye`

```console
$ docker pull openjdk@sha256:e6056e90ecfdaa6f672149b53e39f361200f5a5bd01a6f1c86233f547d05fbff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3f400f848d57bcd965d26ea149892589c815682b963c48e9b6cd8c715b2545fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255063893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a90fe3727b154122ecb49c2cfff56d340967afd5b0911be2ae6a08cf535e947`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b8d280093b43baf35d62386c6ddd10871aad5b47a2e74ff5932b0e7e5c609`  
		Last Modified: Mon, 07 Jul 2025 20:59:49 GMT  
		Size: 1.6 MB (1583608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1cd1b8e395e544ba95d97791788e47ebd2d30f5477bd978669cb8d0b60268`  
		Last Modified: Mon, 07 Jul 2025 21:35:35 GMT  
		Size: 223.2 MB (223224238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f5ec6e25197809d6c84a059d089e137803cffe0f2162368855f7300f95ad1155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae4388edc36168725d9975059febed8ef8b779735eb6aa128520b25d2261e0`

```dockerfile
```

-	Layers:
	-	`sha256:c7c387093dd0f1281cdaf2c2e32d0161bffeec8848fe793f142f4afaf942e3e8`  
		Last Modified: Mon, 07 Jul 2025 21:23:59 GMT  
		Size: 2.9 MB (2942650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c227fae52636f134612b5f1cfbc05962735f06c21f163908cc9a15c79ce5d79`  
		Last Modified: Mon, 07 Jul 2025 21:23:59 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-bullseye` - linux; arm64 variant v8

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

### `openjdk:25-slim-bullseye` - unknown; unknown

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
