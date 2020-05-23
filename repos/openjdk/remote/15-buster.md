## `openjdk:15-buster`

```console
$ docker pull openjdk@sha256:3d16d52f8172bcd89307742fa4cbfbe5cb5476c4a54b619f2c93e2c5d5926fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:1aea092a9563822334b6fcad9f17993b70f00b6ca0299447188e0da2cca336af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329767829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff877e48dca337d31f119c70f6229968733cc2bc88936eb911c7855090b0c69b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 May 2020 06:28:12 GMT
ADD file:fb54c709daa205bf9d04eb3d90ba068db4c34dfe3b6ec0d7691f677286120903 in / 
# Fri, 15 May 2020 06:28:13 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:32:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 17:32:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:59:27 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 20:59:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 15 May 2020 20:59:28 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 20:59:29 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 23 May 2020 01:25:30 GMT
ENV JAVA_VERSION=15-ea+24
# Sat, 23 May 2020 01:25:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_linux-aarch64_bin.tar.gz; 			downloadSha256=912b1ecb8b9329a67c577d1fa3a0391d48d60e3643c95f923f375b03c7ae51d9; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_linux-x64_bin.tar.gz; 			downloadSha256=b1557a00210626792629afdd5a00e01c8939bb701b13475549063c82619e9a26; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Sat, 23 May 2020 01:25:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:376057ac6fa17f65688c56977118e2e764b27c348b3f70637fa829cd2a12b200`  
		Last Modified: Fri, 15 May 2020 06:37:20 GMT  
		Size: 50.4 MB (50391294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a63a0a859d859478f30461786a49c2fca3ae7d89ab5b5ce3c81c54951d30f88`  
		Last Modified: Fri, 15 May 2020 17:50:44 GMT  
		Size: 7.8 MB (7812354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496548a8c952b37bdf149ab3654f9085d721ee126b8c73b16860778be5137f5e`  
		Last Modified: Fri, 15 May 2020 17:50:49 GMT  
		Size: 10.0 MB (9996284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adae3950d4d0f11875568c325d3d542d1f2e2d9b49bdd740bb57fcfc1f6478f`  
		Last Modified: Fri, 15 May 2020 17:51:06 GMT  
		Size: 51.8 MB (51827083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e77013fe29f244314ba9ced8c62b5615de673a1413327ce0d5c27edc88e7363`  
		Last Modified: Fri, 15 May 2020 21:06:51 GMT  
		Size: 13.9 MB (13920351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb09175c50f8ca7e1d2d7c355c4d7809418a0b9628196511e6b3ff00134f2fc`  
		Last Modified: Fri, 15 May 2020 21:06:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9861468b98baaa07913fe5c6e673608716d33c48aa9db14269f1a8f1fb8b444e`  
		Last Modified: Sat, 23 May 2020 01:28:46 GMT  
		Size: 195.8 MB (195820252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7d5ef64bf899cd2dbfd2b1350478342e50f19a061b6e466620556b9bffd0215c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308129194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768559b47012e5ad4ba4c556b613f747dbd5a02ad08398907873db18f06c37a2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 May 2020 12:43:21 GMT
ADD file:be06dd722febf4e72f7e626f70029986a5c75880941cabd553f695dd66bcbaff in / 
# Fri, 15 May 2020 12:43:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:06:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:06:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 20:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 May 2020 01:46:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 May 2020 01:46:01 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2020 01:46:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 22 May 2020 01:46:03 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 May 2020 01:46:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 23 May 2020 00:54:49 GMT
ENV JAVA_VERSION=15-ea+24
# Sat, 23 May 2020 00:55:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_linux-aarch64_bin.tar.gz; 			downloadSha256=912b1ecb8b9329a67c577d1fa3a0391d48d60e3643c95f923f375b03c7ae51d9; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_linux-x64_bin.tar.gz; 			downloadSha256=b1557a00210626792629afdd5a00e01c8939bb701b13475549063c82619e9a26; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Sat, 23 May 2020 00:55:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d23bf71de5e1fea32788576972e233e80db7c51d831ed7edb269102dab298bf1`  
		Last Modified: Fri, 15 May 2020 12:53:11 GMT  
		Size: 49.2 MB (49170530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6b089b3526111514262a58bbb27c5a292d7ef355184883365cdce9a7c61e5`  
		Last Modified: Fri, 15 May 2020 20:19:12 GMT  
		Size: 7.7 MB (7681693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34690136adb76fac1a121f6c4a9b5a63de1def4d65e0b2f99ff84c392ed8244`  
		Last Modified: Fri, 15 May 2020 20:19:13 GMT  
		Size: 10.0 MB (9983897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4287f76f52e4c390d78182615c75d2b3d6a5cd5b2c28dc554707a7cfbfa91f2b`  
		Last Modified: Fri, 15 May 2020 20:19:34 GMT  
		Size: 52.2 MB (52156755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa685e6c93472269ec2414e8565060efb4ab34f99552cdd72144290c7c99143`  
		Last Modified: Fri, 22 May 2020 01:49:00 GMT  
		Size: 14.7 MB (14674128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05238559a48437acdf8d2821a22d6c47635cbc89aaeeeae039f0788f3a41c432`  
		Last Modified: Fri, 22 May 2020 01:48:56 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acc2aa0117b727915468846f127adcb384656ffe1737347aa67d801e39d31fc`  
		Last Modified: Sat, 23 May 2020 00:58:19 GMT  
		Size: 174.5 MB (174461979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
