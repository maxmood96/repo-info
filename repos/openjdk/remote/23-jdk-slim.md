## `openjdk:23-jdk-slim`

```console
$ docker pull openjdk@sha256:11cae8e78a49e8579883834b65636b44ae7f526632a2e10050dbd3e4ee9f2f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:510ed72ec93e128f1ea01a8892a2b41cb7293b2808d7dfb829ccf6e9c69fc486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244623772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9974a4b6fbf76c76fd6b04abd385f597c27a601fc25e461883dea6a16e53b23c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0c1630f07ed763c6bc73eefdd29cfebbc848a6030cc8a48321ea8152f6aa1b`  
		Last Modified: Mon, 29 Jul 2024 16:56:32 GMT  
		Size: 4.0 MB (4016756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bfeaa24d76a86a38960ddb8498b7ca6683a3645a30b04336f831278f0d7a4c`  
		Last Modified: Mon, 29 Jul 2024 16:56:35 GMT  
		Size: 211.5 MB (211480729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:5dc32bb32019a64ecaf39c28d2b426e2e884e7a0e0f4c61f5005568fe0838b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9224ba9f28e6eb41db15919ebad74a1698b04c807f289f5996b5ea623e5190ee`

```dockerfile
```

-	Layers:
	-	`sha256:d9aa72e1ab1604d24d916b0c92a696b936b8afa3d6d6e594034431b3c6619f8e`  
		Last Modified: Mon, 29 Jul 2024 16:56:32 GMT  
		Size: 2.4 MB (2365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6a122fff7e98690b27cab972ac353a7b90b1b05dfc703455f60383d3b0a1c1`  
		Last Modified: Mon, 29 Jul 2024 16:56:32 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:39140fae57c71b26b1ee4d9d9ec83a4fd0fa7f470f424a7c435b6839c0173a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242335047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb57d39978ef6a573559abed27438c99b6ed3aaba8fc7ae36e31579fdb8e428`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c349375e2e294f7eff4dd86f726854408dbf40098a96b9250ed96a5be15a73f5`  
		Last Modified: Mon, 29 Jul 2024 16:59:58 GMT  
		Size: 3.8 MB (3829955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de58cd2f245912949c0efdc28739573dab98e5d41de5248fe73aa46db101dd0`  
		Last Modified: Mon, 29 Jul 2024 17:05:25 GMT  
		Size: 209.3 MB (209348521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:eee3568dff7e5899847c9db885099ead8efb8f6d632c451b4801d1ea1cd82d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad0215b95b4d599015c6de70eb17b8cc1effc067c30fe7278f75bc791ec3ac1`

```dockerfile
```

-	Layers:
	-	`sha256:396ac8ae11e88bd3b7dce3749beb5d29449f52e5241a8d6376e81866d6b57d12`  
		Last Modified: Mon, 29 Jul 2024 17:05:21 GMT  
		Size: 2.4 MB (2365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d28150f285b047ef1399c84b4237806cd993be8c86ce86c3a51533301ef7bf8`  
		Last Modified: Mon, 29 Jul 2024 17:05:20 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
