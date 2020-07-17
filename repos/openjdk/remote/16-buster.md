## `openjdk:16-buster`

```console
$ docker pull openjdk@sha256:b3b5e7f134c165303aebcf05538bb68ac9cb1faa5078115b1e2eeea7ce0c7308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:8f809e1be525b71ab88251f7014a71a22c8b9a8ad9f24b180a58d8bf40fd87fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330458244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a5e442eb12855d9679f91067a34cbda24d93170caa604a57e8e36de7f08c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:47:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:33:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:33:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jun 2020 20:38:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Thu, 18 Jun 2020 20:38:27 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2020 20:38:28 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Jul 2020 22:36:15 GMT
ENV JAVA_VERSION=16-ea+6
# Thu, 16 Jul 2020 22:36:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_linux-aarch64_bin.tar.gz; 			downloadSha256=c9ecf57bfb0f727ed96419f975d018d8205b83f4db1896801e3c96c9b441cd1d; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_linux-x64_bin.tar.gz; 			downloadSha256=8c4672179d1259e172534b062c562b6f70f56ddc4507db0368b52b1483e28c41; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Thu, 16 Jul 2020 22:36:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e6b19a265d6b8b7934e7ddd7dc07f6e2fc945b3a28dda9b8aecb12cdb30e0`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 7.8 MB (7811709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14b6c2f8785723bceb5964c5dec1f0489b7750e9d4ec671e49bfba15d80a39`  
		Last Modified: Tue, 09 Jun 2020 01:59:52 GMT  
		Size: 10.0 MB (9996168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573c4b3094956931fd68c310ae92c9eb1a787f0c77ac2730be9d16cce172d5e`  
		Last Modified: Tue, 09 Jun 2020 02:00:08 GMT  
		Size: 51.8 MB (51827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02beab046a2499f45467129ea69df9958c19b479ce0335f7b3a0c797531363fd`  
		Last Modified: Tue, 09 Jun 2020 16:40:51 GMT  
		Size: 13.9 MB (13920283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6cdedf20709852683e2062dab69161639793ece4a8858f7416a3b41a47adb3`  
		Last Modified: Thu, 18 Jun 2020 20:42:19 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ca73f0c4fc0fd18bf77f2e64ecaeb6b4db7061fdf8f370e95205ad504de58e`  
		Last Modified: Thu, 16 Jul 2020 22:42:37 GMT  
		Size: 196.5 MB (196512875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:174fef59b164f947f0c76c379bd678e763a109f1361a1c06b456c1a4fadeb2b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.7 MB (308728011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19decf7a87e9a2962eef4239cb1628ec4607b86f0652c2573ab73d86ea2f45`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Jun 2020 01:51:33 GMT
ADD file:73f1cc6ac15b24788e78ae41cd6c89cb5211d64baf491accbd95b6fe9718f17f in / 
# Tue, 09 Jun 2020 01:51:36 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:31:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:32:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:32:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:41:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:41:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jun 2020 23:56:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Thu, 18 Jun 2020 23:56:21 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2020 23:56:23 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Jul 2020 22:13:47 GMT
ENV JAVA_VERSION=16-ea+6
# Thu, 16 Jul 2020 22:14:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_linux-aarch64_bin.tar.gz; 			downloadSha256=c9ecf57bfb0f727ed96419f975d018d8205b83f4db1896801e3c96c9b441cd1d; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_linux-x64_bin.tar.gz; 			downloadSha256=8c4672179d1259e172534b062c562b6f70f56ddc4507db0368b52b1483e28c41; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Thu, 16 Jul 2020 22:14:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1db90d3d3b6598d485690f804e96153fb632e7434251d334e9a0c49b773855c9`  
		Last Modified: Tue, 09 Jun 2020 01:57:52 GMT  
		Size: 49.2 MB (49167914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e848fd373270c8ed6d276649dd8a5860d188f7d0ff306e91e4e3e092e541d99`  
		Last Modified: Tue, 09 Jun 2020 02:47:16 GMT  
		Size: 7.7 MB (7681351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c85f14a5d8064020366c03aa05ec1c8b0f731e0966bb9788960d27258634aef`  
		Last Modified: Tue, 09 Jun 2020 02:47:16 GMT  
		Size: 10.0 MB (9983910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334e38f2d6fff7c08f4ad1b38ec441d2cf963b761b5d85983396a75ff6d0c08f`  
		Last Modified: Tue, 09 Jun 2020 02:47:41 GMT  
		Size: 52.2 MB (52156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11155943d47fc5419c4fe245424e1a06a7cf33a8ed67385ad65cf6508f86ea53`  
		Last Modified: Tue, 09 Jun 2020 13:47:52 GMT  
		Size: 14.7 MB (14674134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da529403cfb69520ed432ff2243f1ebf8cc1a6faef8a67b526c245a752740cb6`  
		Last Modified: Fri, 19 Jun 2020 00:00:10 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ffa49792f54f30601316221f1a92d029628d18af770121696ecfdf38be519`  
		Last Modified: Thu, 16 Jul 2020 22:21:42 GMT  
		Size: 175.1 MB (175064234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
