## `openjdk:24-ea-20-jdk-bullseye`

```console
$ docker pull openjdk@sha256:3251a89be7ed443086ff633f87f042a1e26c772a00786e06ca19a16166ac9666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-20-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:718dee7e27b3787a9afeac7b8d0ce05726f292d782771946b14c740ea272cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352176927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e2606343b0b9067813182bceb089744b4e4e3e887337d7a77031507f0bf153`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 18 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+20
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='b7a84616949bac4a00a9a96d771f6595e7fed371c0a5a54139285311e4c0b367'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4fe26b4900462d35fcaa9c7b551fd23791906f05eab3a609de8d771cc15ad9d0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac934cf6d47cf19df964df1faca0c3d8aa3a636a6da3e3a5531e59fda97bfc5`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 14.1 MB (14071339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e708b1b2cad1575263895c1b7d7c3ce6a26655689015a78e6c2f0d1aa73b55`  
		Last Modified: Sat, 19 Oct 2024 02:54:44 GMT  
		Size: 212.5 MB (212537376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-20-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3510d0f7463feeafd56d6b969db65dbf041979c92dd57906d7a3b03133aab158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b23aa5d10ae60521dd0b313f79460e49061e4ebea6fdfc39ee2c47456a642ce`

```dockerfile
```

-	Layers:
	-	`sha256:9579609c4fec942f9b07e1d8e127732156d2475f2dbc10c00152a9940af8b745`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 8.4 MB (8355822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124ae6a38d2c60116318b7e02edeebffb4b0e79b3f59500b168922f4ce14504d`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json
