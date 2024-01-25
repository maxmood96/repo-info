## `openjdk:23-bullseye`

```console
$ docker pull openjdk@sha256:d291d8f42718e7b065f412f1270bb08612f4c81591908a8a59f80b4b227d1a4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:2b80dad0546418e1c1ae116c446936293d31a87a0c68d3ccfe4606b86d8b7902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342668189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8083081878c97b6df741e0239d40b47dd0a35afd148ba6840729b441fabce933`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:32:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Tue, 23 Jan 2024 20:18:23 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 20:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_VERSION=23-ea+6
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='5163a8a077bfb1cb60e6b4ade06959b0ecba73399a509a5e83f8f9df5cebd140'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa7e954bb29a17c5d0095c4ce94275bfe53383cb8aa7f14894d352e9c00110c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24098c8d74fae9a314e70517566e785db7b39341cbc4bd63adf14c330728677c`  
		Last Modified: Wed, 17 Jan 2024 02:01:11 GMT  
		Size: 54.6 MB (54601537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020090de1d2ac9113b04b94e2caa8fea33ed8c63d54da99c0e5ff70947d77f04`  
		Last Modified: Wed, 24 Jan 2024 20:57:04 GMT  
		Size: 14.1 MB (14073090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44956337787f109c7ce129ba9e876ae78fd724159d7b9583c0b3c4cc4269afd8`  
		Last Modified: Wed, 24 Jan 2024 20:57:09 GMT  
		Size: 203.2 MB (203170726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:1950459cd7ee7a9b61f04654d1ed9e8bc1202dd864495d2a9a40c1796cad2c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfed6c80627c71b6f49e355a8e9d3dd50155c4f555b48670cd7d363fccd8a1fd`

```dockerfile
```

-	Layers:
	-	`sha256:9e278a65c6f37498155ed147f317009ed363120170dc27e4c6def4ef9c6c1724`  
		Last Modified: Wed, 24 Jan 2024 20:57:03 GMT  
		Size: 7.0 MB (6956076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba5b13dcb400ded17532b629bea3ce4c092be83e49f6d83b559ca4ee3992468`  
		Last Modified: Wed, 24 Jan 2024 20:57:03 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a40f5961161a31d4d4e02d2e8ad8e1cbf65a58e1754b0b39028a18fbc0ba7277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.8 MB (340767916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fba472a20016e0c547c47254fdddc64ce64ee4a1edbfe02c105d0c1190d20bd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646806c0e22a1bfa60edc42bcc6170f0ccd02431e5871b9cec1962c34d610232`  
		Last Modified: Wed, 17 Jan 2024 02:59:33 GMT  
		Size: 54.7 MB (54699826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6597735fb25c8c3b45d772b2ab6ae70d0a21d14afa3336d928cd67e8eeb328d`  
		Last Modified: Thu, 18 Jan 2024 03:39:02 GMT  
		Size: 15.5 MB (15527417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bc6e9db708e560a9b4b9d04dca9eeef1e264571be1b67100e23ce235d7183e`  
		Last Modified: Thu, 18 Jan 2024 03:39:06 GMT  
		Size: 201.1 MB (201082115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7db87ce3b56be4d86504f4da595e4817c38446604cf794c7081ba145dbec6ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8150ea016dd9c1bf150f0a8299a4d236f612c363aad1416cc97abcb5a271cbb6`

```dockerfile
```

-	Layers:
	-	`sha256:7b899df14d65d9d00f257b85bde7764e05bfb5b0aa44d9c131a42908d3f4dc05`  
		Last Modified: Thu, 18 Jan 2024 03:39:02 GMT  
		Size: 7.0 MB (7043728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8371ffc1be2ab17d5b736e1df95b7d03badb36b664b89f069d01de201669883f`  
		Last Modified: Thu, 18 Jan 2024 03:39:01 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json
