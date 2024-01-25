## `openjdk:23-ea-6-bullseye`

```console
$ docker pull openjdk@sha256:a014a03e64cf6844dcc933f957c49dd9fc91fcf392c552db01b762116ef377e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-6-bullseye` - linux; amd64

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

### `openjdk:23-ea-6-bullseye` - unknown; unknown

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
