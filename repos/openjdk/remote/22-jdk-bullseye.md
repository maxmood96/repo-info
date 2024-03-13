## `openjdk:22-jdk-bullseye`

```console
$ docker pull openjdk@sha256:4a9fce629ff3ed8387bc9844bae0181847944c4f88b395909ba97d391b3940ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-jdk-bullseye` - linux; amd64

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

### `openjdk:22-jdk-bullseye` - unknown; unknown

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

### `openjdk:22-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c806d234a4eb95f91fa8c2e40a15f25425f66a32a5be1b30d2a74544c3b1b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340624897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7829983eb33e968f50326132ce462d05b6aae5270675751168c7356a0d0a2aaf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Feb 2024 19:48:24 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
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
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f751cb4b7796cfbcfaae20e0b3e0c200c54d01e07ae9efe020b2a38d5964033`  
		Last Modified: Tue, 12 Mar 2024 22:26:35 GMT  
		Size: 15.5 MB (15525961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5e103c0b358010b4da2704b0bbcef3a47c30d448fecee1b41ab0eee9b69e`  
		Last Modified: Tue, 12 Mar 2024 22:29:57 GMT  
		Size: 200.9 MB (200933333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:dffecf97ee6db8d1edf4adeed384d45e532818d5d328bdaec794cce49502509f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8275851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3512253b8874cbecbc8bcab4618694806dd4aa7ebde980675314bd9f4f41653`

```dockerfile
```

-	Layers:
	-	`sha256:4479e0e929bd7f0976ee89963f8add0ffa29176f5ef5bf440dbd4b82aa1fe0d3`  
		Last Modified: Tue, 12 Mar 2024 22:29:53 GMT  
		Size: 8.3 MB (8258020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e4886dd8a6d781d901353e03b1202cdb19a7ec51b2711a72c05cb7841d7174`  
		Last Modified: Tue, 12 Mar 2024 22:29:52 GMT  
		Size: 17.8 KB (17831 bytes)  
		MIME: application/vnd.in-toto+json
