## `openjdk:24-ea-32-jdk-bookworm`

```console
$ docker pull openjdk@sha256:a0a747cf5df08089be8d86d5e533662bf449524e6bfb87e44e64562784f68f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-32-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f9fd3c3bf824e76f09fa56ee520918c3f7ce89bd2eb0a39b844fdc629964d143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366775258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5382e1de41a15348404b15cb35fab35735d11e78fdde249544eabfaee5282b3a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fefaaada127084d49d74576f264a838eb7b56f13cdb5df7b5ace5a909dab3bf`  
		Last Modified: Thu, 23 Jan 2025 22:26:38 GMT  
		Size: 16.9 MB (16943079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad5a4bf397c0e19910b61253b7600c1808fe2f2c8c8c39cc4a7e0851a4a6a3b`  
		Last Modified: Thu, 23 Jan 2025 22:26:41 GMT  
		Size: 212.9 MB (212894894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-32-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f3ab74383ed6fc1408616c71ecba0ad0d3a314d228d6aaabdf350e2264098ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8454869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ceb1bd4005ee7009864faf3c127e38bac40afa80816a5f783a310afa6414963`

```dockerfile
```

-	Layers:
	-	`sha256:b52950a74fb493ac1bbf9910a08297a0c27555ece3f16a607f3b88d96619e2d1`  
		Last Modified: Thu, 23 Jan 2025 22:26:38 GMT  
		Size: 8.4 MB (8436252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef83e6233e1a1b7b4f6422d91a25b2802939c511aed9b430ecaa8341da51ac2`  
		Last Modified: Thu, 23 Jan 2025 22:26:38 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-32-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e5c1b51861c07ea8e9955a58ee5ddb33005ea63fe924abca9eac6851fc96c54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.8 MB (364835359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1edbc796728606a91563e8e15067c744f23cf6f6e7a47ff9c7aeb357ed4c3c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6a2555d05d59a1b517aac5c56ae999793d8ea02a417f7a16f4c8c2080cafbe`  
		Last Modified: Wed, 22 Jan 2025 02:32:06 GMT  
		Size: 17.7 MB (17726678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5f285c8f12a9bb33151e3c8b5b347f55324d74a8ce99844f3ed7aa771b1c34`  
		Last Modified: Thu, 23 Jan 2025 22:31:51 GMT  
		Size: 210.8 MB (210847127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-32-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:97594c83f479327cf964e8ea56117f0cf5276210b8848a56d59a6452cc8d7aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8591881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6194e6ca5c30c78e624ed356da28c9dea5f8c139ecae4baaf774b853232f57d6`

```dockerfile
```

-	Layers:
	-	`sha256:8b924b3ba8785c0dc896e9304184c0de353c2ba2e9d0e3944b29e998bfc1030e`  
		Last Modified: Thu, 23 Jan 2025 22:31:45 GMT  
		Size: 8.6 MB (8573120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c92aec9896304ce2a40046c165b9adc5b821c4ae22605bd71ced90ce6a011841`  
		Last Modified: Thu, 23 Jan 2025 22:31:44 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
