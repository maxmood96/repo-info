## `openjdk:27-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:86fdafb2335396fbc7c9312bb93ec43a374e9d1034ae22433cc5c762020e962b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:01288b981cf28054c140bc24e55345fb6cc7cd182499a233fd557f58a8f1c2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382476246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44abf62d8cc5e7b54dc7a3203fe7bcd88333342412afd7721e876b138d4bff96`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:52:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:52:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 30 Mar 2026 17:52:52 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:52:52 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:52:52 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:52:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:52:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb77bc07c5582365e270cd096683a1a4130e8bc4f894b9535e05754acb4f990`  
		Last Modified: Mon, 30 Mar 2026 17:53:16 GMT  
		Size: 16.9 MB (16945136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3116dd133ca1cb0ee7751c8f05cd49206518c92b53360bc5377b07601c66385c`  
		Last Modified: Mon, 30 Mar 2026 17:53:26 GMT  
		Size: 228.6 MB (228608701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b415b00e36ca53a4dd4b964e1616fe702171627fd022907225d9cf0267cb5552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f7b946b16d14a51c19c22fac0084055123220af724bb22940d37d8de80f717`

```dockerfile
```

-	Layers:
	-	`sha256:1f99f0624294d6ad5868b2aad58f394ca41c78361bdbe55df4d824a437201c48`  
		Last Modified: Mon, 30 Mar 2026 17:53:16 GMT  
		Size: 8.7 MB (8668887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14225bc54172d42afc95bb0e8129ef2bafb557713566b00c18a92d7f40723c9`  
		Last Modified: Mon, 30 Mar 2026 17:53:15 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bdbc35c0afdac835acf3874ac00c9011d31bd2f10f9f290387f14400b7c240d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 MB (380756906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c609cd0d4bf75c23ecd1ec14889ea8ff9760e0f0d9f557c1e4578ce19f3724`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 30 Mar 2026 17:49:44 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:44 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:49:44 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:49:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:49:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68d06949a111dcec9de02f66afe2af316533b445db9267ff533126a6c5b1737`  
		Last Modified: Mon, 30 Mar 2026 17:50:09 GMT  
		Size: 17.7 MB (17729169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58b6fb2a3412431eeeb6e3a678e5da762fc93f3dd2f1bd64bc90190bb491f81`  
		Last Modified: Mon, 30 Mar 2026 17:50:13 GMT  
		Size: 226.6 MB (226570562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:244ed5da9d30f61314484138f8dac0ba6350e7350d5cf2b7ad90a0f920a8a9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4416e404d963338abb971211ad1f1d818292cb93e2bf565e4e4888b5d76f30`

```dockerfile
```

-	Layers:
	-	`sha256:f0429cd69b11cd5f975a5d911d1a9ce41c6352b8ba4a2cd80ef6c54dd2d2318c`  
		Last Modified: Mon, 30 Mar 2026 17:50:09 GMT  
		Size: 8.8 MB (8805732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04998879994d82c1c3c9997daa9c0f38467e96777350a7ef9ee6995bde86bee9`  
		Last Modified: Mon, 30 Mar 2026 17:50:08 GMT  
		Size: 18.1 KB (18057 bytes)  
		MIME: application/vnd.in-toto+json
