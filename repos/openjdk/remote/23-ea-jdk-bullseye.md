## `openjdk:23-ea-jdk-bullseye`

```console
$ docker pull openjdk@sha256:582cbd8bed2def100075ee3424ba810e67457164749f78456ca5daf5ffb34b79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:beeb346c92d8a3246cf63ce7afb7a7a224d47a800a797413e60a8210cd23f196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342665585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c21eaf74338adc9d4dbdf0c5161cd926273a8a1cfe1b8979e23e693a6061b1e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:37:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c23b7d6528239a16f11d6e650e9a9fdb7039721df42b6ca01777fe34c2b116`  
		Last Modified: Thu, 11 Jan 2024 04:45:57 GMT  
		Size: 54.6 MB (54601205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08662416ef1023ac12e726d811a904c908ebcc436b3a04996b47243515c410d`  
		Last Modified: Sat, 13 Jan 2024 01:07:15 GMT  
		Size: 14.1 MB (14073070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e9fa84a576c1216351e5e6172a4bec56ac132b5b327bfda4161feaf0f840d`  
		Last Modified: Sat, 13 Jan 2024 01:07:18 GMT  
		Size: 203.2 MB (203168474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e43de039f73ad58ce18d4df0f4a10c3d88a9a255be914d322d8b04dd28bc93e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81168251a5c45bc5af62cfe6f2b7e7090d65a00db929032e20c926463f8639fb`

```dockerfile
```

-	Layers:
	-	`sha256:b627a486084be8d0d1fdf84d4a59a1383830a0ff2f81288879f36554ecfb485f`  
		Last Modified: Sat, 13 Jan 2024 01:07:15 GMT  
		Size: 7.0 MB (6956076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92b92494fc63ca81e48b28e64da47833efad778acc1adc63700e88e4ceee6c3`  
		Last Modified: Sat, 13 Jan 2024 01:07:14 GMT  
		Size: 18.9 KB (18889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f16562411318656526e2933866fd1bb79a3601c12073229deaf7add0c3160a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.8 MB (340767890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0821537d1313d918e7d939a5406110b984647165a037eb06340583711b0363`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:26:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:826044e8ec1545c4af5dfe71ab63bce600198330f150aa968074bb86e78cd154`  
		Last Modified: Thu, 11 Jan 2024 09:35:17 GMT  
		Size: 54.7 MB (54699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bfdfb22779e890668f0c60388a356f85eebf1e6ec064809ade715ec6947048`  
		Last Modified: Fri, 12 Jan 2024 09:22:42 GMT  
		Size: 15.5 MB (15527396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be431e23d9716a00fec13adc51bf56ae992e2e2f1592dd5ae69fbcd28f795f1f`  
		Last Modified: Sat, 13 Jan 2024 01:41:34 GMT  
		Size: 201.1 MB (201082067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:03718cdd012bc50b5fdbc262ea354e8b7d84d297d5ad1f9ff1c546ce332ea9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23c10315c8237f67132412168aef4b47262627bb5b80d2568b13bbb927f2237`

```dockerfile
```

-	Layers:
	-	`sha256:f020e5a9de27df9f8e68a5172a8d4667ace8f8cd46ba6bcfa15913a5105035e9`  
		Last Modified: Sat, 13 Jan 2024 01:41:30 GMT  
		Size: 7.0 MB (7043728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c5b617360611218dd21ec0bf40213166b691287b51e3b26e92c2cfd0aa1545`  
		Last Modified: Sat, 13 Jan 2024 01:41:29 GMT  
		Size: 18.4 KB (18407 bytes)  
		MIME: application/vnd.in-toto+json
