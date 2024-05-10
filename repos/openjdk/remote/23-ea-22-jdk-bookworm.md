## `openjdk:23-ea-22-jdk-bookworm`

```console
$ docker pull openjdk@sha256:d6169f11fec818a60caae38f5be7995fdff30a4d4f97def82135fbc29b76acf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-22-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0191f9136cf952a5414b43534af6707d01f9ce0572c4ee445cd50c7080dc8d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364738054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d51bf3e58102f00fd05b1f85bd7dedd2a0a3c1cfac3c3d1530f96563372d39d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b9edb6364d71bcd8187981d6483fe74c1053112e0142996f9ff70e64b6b98`  
		Last Modified: Fri, 10 May 2024 00:52:46 GMT  
		Size: 16.9 MB (16949425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2f9708bd0919c1bbf3660685d5ff2dc012d4b0cbaf4892299045fac8c6dee0`  
		Last Modified: Fri, 10 May 2024 00:52:50 GMT  
		Size: 210.0 MB (210020088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0208314dcf32c9644a3647e7946924b1011043efeb201615709991baba036fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68847fc314073aa82d8c96050c10851189eaa4db09a0dcd7841f970d090c0505`

```dockerfile
```

-	Layers:
	-	`sha256:68b2d4de0749d12867befe3b4e3021866ee15ec03463177803a4776db1f8c1fd`  
		Last Modified: Fri, 10 May 2024 00:52:45 GMT  
		Size: 8.2 MB (8221828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58eb2b781e0965f779adef9f4d414526c99dbe09951a241999dde3dd1207b579`  
		Last Modified: Fri, 10 May 2024 00:52:45 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-22-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6b4a885156da9ebfeb197169bcb95e1bb0ca8f7589254d56a1f6b80cc0cfbe58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362836235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a795969b9070ab843dd90881c995631407dc54471c40f2d18efa89b31ab3198e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16eba34c2918e888cf329436d3d8c4a1938b79364d7daaa9a075544f9c82c24`  
		Last Modified: Mon, 06 May 2024 23:49:34 GMT  
		Size: 17.7 MB (17732569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a04d56cf477a1c40c90dfeb95e730f4be7a4ee747ea8e132e28e03d98a8a59e`  
		Last Modified: Fri, 10 May 2024 01:15:33 GMT  
		Size: 207.9 MB (207908724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:da47f8e05e85b5c03be0a560a99854fa92c12c4b1be034dee85c4f7e57456b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed214bc9f635ac21c566e36f9121b580d44e2ecdd1b0009119429bc4e508817`

```dockerfile
```

-	Layers:
	-	`sha256:cab532059c4c0652c4f1411ae9a5ef62064245f8be070990b4722c5e49e7443d`  
		Last Modified: Fri, 10 May 2024 01:15:29 GMT  
		Size: 8.4 MB (8359424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce173524f4656b1ff9304ac88b2f55046c609cf39ac594802decd9aa7c50ad94`  
		Last Modified: Fri, 10 May 2024 01:15:28 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json
