## `openjdk:22-rc-bullseye`

```console
$ docker pull openjdk@sha256:7e8beeb79d3f3dca62edaecb5fb3e375cf58ffe3b50e4a0f7bcdfe9c71bd36e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:739bd174cef140eeec784ff16d31df1cfaf06252ba66679158a04f9b7488efe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342381893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0819a4d68c391d63239dea0b817c8ed1cababae12f44bbc99e3aa3b045cd61`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Feb 2024 19:48:24 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6715d714c0b7c940c4c11daa67519b8ef0656a3d802509f63d5dcd6e4612952d`  
		Last Modified: Tue, 12 Mar 2024 06:58:12 GMT  
		Size: 14.1 MB (14071297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073133592c00f8dc7f3397de7157392fd1d237bf7bc795a53849326e9c91619d`  
		Last Modified: Tue, 12 Mar 2024 06:58:17 GMT  
		Size: 202.9 MB (202873664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e6ec0dac1574268db87f7fedd3f5d1c8d53c230ea23b448aae03782b427c880a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1862208c10acfef38889579983e35362469fc89a293a51dc56827158b3f24e`

```dockerfile
```

-	Layers:
	-	`sha256:7c5aa36cc432472891ba90e998bd795940cdacf1fcdbbbcfb04c0b34379bbba6`  
		Last Modified: Tue, 12 Mar 2024 06:58:11 GMT  
		Size: 8.2 MB (8156377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4222cbba8d22c0d24876621478ed3205a238dc9626a638e65e375a15b46b41`  
		Last Modified: Tue, 12 Mar 2024 06:58:11 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3a55443f8aab7904a727d2bb322311a3014b028042005b6012dd83264c84f2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340623520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3430f21b480c3b62cc989e94652d88727ed3258274a843bdb5c47d9f982e4b8b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c2c85b768f52fc0353f0af0e43d671b1d1025996f39d238e750611070d206c`  
		Last Modified: Tue, 13 Feb 2024 01:47:53 GMT  
		Size: 54.7 MB (54693679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4e7e2653db67e0f48166dd6ea745ba3c9b5723f8ad79a1592ac1d137a2420a`  
		Last Modified: Wed, 14 Feb 2024 01:17:21 GMT  
		Size: 15.5 MB (15525873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c2383bf3da8d71953898a80106df89593f092d09e717a04085d1fd5d5d8ef0`  
		Last Modified: Sun, 18 Feb 2024 05:24:33 GMT  
		Size: 200.9 MB (200933341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:739a6fc75bbfdf56ee8bd1b9752cf150e22a76813f9e48bee10a97036325321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8275852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b265f502b51ca6cfb3e85aae283276cf972beb9804c3558de550f8ff9f8c44`

```dockerfile
```

-	Layers:
	-	`sha256:045a1aa2beb8d6ceef1b9c9e22d5bebf4991ac855c7d4f2ed8949330fa480e22`  
		Last Modified: Sun, 18 Feb 2024 05:24:29 GMT  
		Size: 8.3 MB (8258020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22918cdc845a646a25f23250bb8d8a2607b64ce2690bfbf2637c2eacedae1d45`  
		Last Modified: Sun, 18 Feb 2024 05:24:28 GMT  
		Size: 17.8 KB (17832 bytes)  
		MIME: application/vnd.in-toto+json
