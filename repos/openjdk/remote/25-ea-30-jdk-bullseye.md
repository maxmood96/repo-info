## `openjdk:25-ea-30-jdk-bullseye`

```console
$ docker pull openjdk@sha256:1769a61ff0dffb21773561e1be711c9ac87760c3f3e2724c0154b0d8055d627d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-30-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:f232b39d3dc29aeb3e25ef31901c7b39e35cdbad1d1fecac1667886efa9cf503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361523805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3fbf9d8c42b26ade994ad30c74820fae3407a352b075dcdb519db3fb92575`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c6a6aed13fcbf08ad442237e89c7c82c4e0c0bf8ae2c6ec82d7954a64ba1d6`  
		Last Modified: Mon, 07 Jul 2025 20:59:50 GMT  
		Size: 14.1 MB (14073108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774d61f3a522c608b57580155dd8baacbcc964abc0e0274448bf2ce9c40cbf1`  
		Last Modified: Mon, 07 Jul 2025 21:42:43 GMT  
		Size: 223.2 MB (223173058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-30-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e6b8c6ecaecd7349dba83ec6deb4ad82e38d9c1379c9c76873acbd3eb50262bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ceaaa038237591d617fd2269f10fb818b12df85c616781d2e65dfbdadc1d44e`

```dockerfile
```

-	Layers:
	-	`sha256:45576f96e980c1c60761fc6d3b345a74fac32cc4f00cb63dbe70dff11b3a1b62`  
		Last Modified: Mon, 07 Jul 2025 21:23:29 GMT  
		Size: 8.6 MB (8590832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63bb7dff09c2cb3e45805b245f174d7a80d99a54943aef4edcac7fea1a7ffead`  
		Last Modified: Mon, 07 Jul 2025 21:23:30 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-30-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:86b0e60ad13832ef9816cd1269e87d522b039c9576602d252b6ca476908f31c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.3 MB (359348101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73aafb4fc646c07b8ab7f787aff66f68a5edfee13d5c5a1f4307521ade740d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adceae3b84ca18cd443e9edabb2b5a26391baa4f5ea48ee70108f934fc1ab0e`  
		Last Modified: Tue, 08 Jul 2025 02:08:28 GMT  
		Size: 15.5 MB (15527655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a340cd06410d931c04af26a4d6da8900afd176d09a6ca584fce4c1d4a0cd60`  
		Last Modified: Tue, 08 Jul 2025 14:08:20 GMT  
		Size: 221.0 MB (220961754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-30-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d8bf3589e6aae05e656cad71fd92560c5235ab7a9f04291bab88e4e4a0f1b743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8710556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f5cad62cba725d40856e1d845815c9220ded9d35e5d2963c112e04100c6e6d`

```dockerfile
```

-	Layers:
	-	`sha256:a86292afe2ba45e0df8e93019d54f7c64f6f0624cc7a9dc7c9b2ff356934df9e`  
		Last Modified: Tue, 08 Jul 2025 03:23:31 GMT  
		Size: 8.7 MB (8691795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec86578d52abc7f571cd30cbc3690b822cf0663d7a8d4689baf49b50a8e5dbdb`  
		Last Modified: Tue, 08 Jul 2025 03:23:31 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
