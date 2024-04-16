## `openjdk:23-jdk-bullseye`

```console
$ docker pull openjdk@sha256:c00672ca4b38895347d13a29c4c13ffdcb7c8a1077297afa9d3f75da55bef495
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:ee701718e9c90b611f8ffa63ab82c836c37bc798faae9c1d10f56665f7a3f871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350479774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a9d80aea05fcf886dfe5f369782f4a046d30f049dd4c43af0c83d5ac670ab8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f175b2b4524fd52eb7952bbb3247866ebcf4b5af2dd22175307f7074d334e`  
		Last Modified: Mon, 15 Apr 2024 17:50:51 GMT  
		Size: 14.1 MB (14071298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821c92090fb78724e615ce6d5ea3ff6d96653cca16d52fc4ba2b420e197db077`  
		Last Modified: Mon, 15 Apr 2024 17:50:54 GMT  
		Size: 211.0 MB (210965951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:803e59ecafc0404d9af94743758c39cb0c295efcd591b0c3c4ec3bbae2d412fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7938551b46f6a6bc3c82a6edd271e95b8cf5871a97f73b27b42b44c15044cd`

```dockerfile
```

-	Layers:
	-	`sha256:59a26cda44dfc70ccfaf29784bb934c03ee89d62d31504dd1dc6dba497b1848b`  
		Last Modified: Mon, 15 Apr 2024 17:50:51 GMT  
		Size: 8.2 MB (8157041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e28f2f9a47fa256a64d5918b11114d7d315d404de5f1763c3deb41979201463`  
		Last Modified: Mon, 15 Apr 2024 17:50:51 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:480e78f39686b54dbb8016a88db96fe519ecd9127ee8e24c71328b411e229cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348547585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29185837946624f32cbf687a15bd8f071044d10f6fc15fb30b6bfebb3a3b1e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27317b8832e116e0457de89bfb9097cbcd3165d6079c38230f3728894dfb3af1`  
		Last Modified: Wed, 10 Apr 2024 04:33:14 GMT  
		Size: 54.7 MB (54694342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f7c38ba8ff505f8ad747931cf34e37feb8500c426376a33971a9956963ec7`  
		Last Modified: Thu, 11 Apr 2024 05:03:41 GMT  
		Size: 15.5 MB (15526172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc650585f76170d76c8ab100cf1f325bd68f75fde5fff60a7d2984be70f1f8ab`  
		Last Modified: Mon, 15 Apr 2024 20:23:23 GMT  
		Size: 208.8 MB (208848656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9c31052658b850fcc8af260d1114433e825720601e68f41cf293a7682803bd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba765a41e2d374ef44c7e3eed1727f0cf35ae588d2482e1b5895f4152bc460d6`

```dockerfile
```

-	Layers:
	-	`sha256:d7946d06921be27567bac74ff8290f01be00dc778f5640a38d5457b3ac361b53`  
		Last Modified: Mon, 15 Apr 2024 20:23:18 GMT  
		Size: 8.3 MB (8257727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59dee91b2afad22b389d0f1bf30a4833dba2e4bb2eaaa4668c822389ecaadec9`  
		Last Modified: Mon, 15 Apr 2024 20:23:17 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
