## `openjdk:25-ea-2-jdk-bullseye`

```console
$ docker pull openjdk@sha256:2f2454e504da3258a0fb4268cb25ff1badee3b6e74115fcf97c589ac0a528889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-2-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:8cc1b579be352363b038cd6fca62b12f0c45b78c9944ee950be44555e77489f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351095980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4de0656460d29f9be5a4c9db89790ef9e07bc46e67f85b4b93826fd80425435`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71d7a744a1440175623affbf8f34d519b9ed560a22963a46111a10c8bc68787`  
		Last Modified: Wed, 25 Dec 2024 00:13:51 GMT  
		Size: 14.1 MB (14071405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a148a1d8edcf78866e1ddb44cb95c7f80cd56ccdd9e4d16b14a2ab326df973b0`  
		Last Modified: Wed, 25 Dec 2024 00:13:54 GMT  
		Size: 213.0 MB (212973617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-2-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d084253a6b48be680b0f3a61470e7f6696ce935717aaf06fde816bad91607734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785315c7f5c9be08f1c93590229a7786175795815524084204dd2b446f599b85`

```dockerfile
```

-	Layers:
	-	`sha256:f358787e371baf0f95f7cd22038a2d14381ab70a2cccca63b6382186e97a9ed9`  
		Size: 8.4 MB (8364777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ddc5455dbfbc4a9039a78b37909a18d35b3f5b86c77e5d6c04af6a62f665579`  
		Last Modified: Wed, 25 Dec 2024 00:13:51 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-2-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:89afc7f360ec941ffa46286b370d73447139d96a777d3fda4ffa20a64758c3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349092185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d68b91f8d7c0c9f00c35c2000e7388de2b5465d985b08a8e540ad6adf2710f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43843d4db248bd55b162c50c092e0af24e1906957688ece77c8fd78e7c62441`  
		Last Modified: Wed, 25 Dec 2024 11:59:36 GMT  
		Size: 15.5 MB (15525945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c07d6d22741ce4808be37dbb0abf6a0ed43625c9b519a16a68c60f41be9e78`  
		Last Modified: Wed, 25 Dec 2024 11:59:40 GMT  
		Size: 210.9 MB (210924093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-2-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:b338c0d72bb976bf68315ceaca43f96f05e7c0c89577324e4397d05d7a564293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8484482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eb05683790add5b9e15d2c77d0f5ab9136a73a93a0066d0b0e8709fd2a289`

```dockerfile
```

-	Layers:
	-	`sha256:3f9732b58ca0477b8f6a8069678e3e9b42d37704589389b4df60ec2c5eeffc54`  
		Size: 8.5 MB (8465739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da8cb72a50e96fc68060848780b90731687cc31a8f8ae51954c99421663983bc`  
		Size: 18.7 KB (18743 bytes)  
		MIME: application/vnd.in-toto+json
