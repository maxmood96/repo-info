## `openjdk:23-rc-jdk-bookworm`

```console
$ docker pull openjdk@sha256:aeaf60f981df3b35b21939ae74679bb99d804069a63bbeaa21278a49dc67b3f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-rc-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e485eea6a2b3cda7274c33af468a41c0301ac19c589af68a935c6278c05dc34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366101542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33d27c37ba258cc094affef69214e29c2ade99dd57d49f7b9504b70cfbcfed4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df05a930cc1525aa6c8dcc5a1864de34ece38495c293c713de1f3ce84d8f9aa`  
		Last Modified: Thu, 05 Sep 2024 00:17:15 GMT  
		Size: 16.9 MB (16943070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66478130713a749d1c93adae28bca2c250421132539da0b0fc3cd6345df7e66f`  
		Last Modified: Thu, 05 Sep 2024 00:17:18 GMT  
		Size: 211.4 MB (211400599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:783143d863fe53682ba5092e84ee8526e86341437bccef6cd2398e5e69cbcdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8274590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e66856a335874815efd934be5ef2fe8109710e0711f565b970f9cf996d2110`

```dockerfile
```

-	Layers:
	-	`sha256:23055b194eac509b0d9f731fb944d66aac6b2bfaab7dac12a24a324e21e35ec2`  
		Last Modified: Thu, 05 Sep 2024 00:17:15 GMT  
		Size: 8.3 MB (8256715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a29c91a5c97bd3f13ebd82b838f3d28770815e1f28b0ab5cb9c5276035dba1`  
		Last Modified: Thu, 05 Sep 2024 00:17:14 GMT  
		Size: 17.9 KB (17875 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-rc-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:810dff9c0a539f588a35aa2baeb2ddf64d4be92db6d5572707099f344d7228be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364188300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a95d38d3d5d04ff3f6fcc60d5d4b781922f05294c37036ec8cd9239efedf37`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9abf6f7aeed04252d2334ddb555665db4908dc6e1eccb0efd47b3a80b410f3`  
		Last Modified: Thu, 05 Sep 2024 12:57:35 GMT  
		Size: 17.7 MB (17727088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc15c6bef40bf1148bc8c8f26abc9574825aa6bb5084a489a70570ed573d5223`  
		Last Modified: Thu, 05 Sep 2024 13:01:43 GMT  
		Size: 209.3 MB (209283843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b047e120f86e7cd307a81fedde62307861b3d8bf8670928ccd8bf5b9320b7c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8412543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6eb451e0de27eab515092269486f5ef296f8c547b1ebb02df84cc2268d2653`

```dockerfile
```

-	Layers:
	-	`sha256:0f1b0b761121a523b3d743ed950cd35da8673ee5f87ffb0523410e1aed55c5aa`  
		Last Modified: Thu, 05 Sep 2024 13:01:39 GMT  
		Size: 8.4 MB (8394352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cb29168ef52be872682fa64936ca45fa920b65863246b746d96606a0a044d6b`  
		Last Modified: Thu, 05 Sep 2024 13:01:38 GMT  
		Size: 18.2 KB (18191 bytes)  
		MIME: application/vnd.in-toto+json
