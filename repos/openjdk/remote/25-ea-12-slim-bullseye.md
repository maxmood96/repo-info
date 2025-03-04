## `openjdk:25-ea-12-slim-bullseye`

```console
$ docker pull openjdk@sha256:72369dc7c1f0505a9184e9a640ce4268d5d5f737ca7f35d032301bd909182a5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-12-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:17ebcaed91b3bb5a33c67784337556771233257c49007139d55b83c94b5d4b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243581094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59949f3f7875ab323f13d0478d68717ee4d795c9a848d5dbe9afbc4b371f91bf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59fcbf3a02bfc8f4b2db2c86f2a7ebcd334b19b2df9a34a3839b33a5f778803`  
		Last Modified: Tue, 04 Mar 2025 21:57:02 GMT  
		Size: 1.4 MB (1377271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0656b4ed23050251653692e67846c1f693057fd9e40ad497335612a4ca846b4`  
		Last Modified: Tue, 04 Mar 2025 21:57:05 GMT  
		Size: 211.9 MB (211949893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-12-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:24ff305f5a6422c484ceea32c43b037e734b36e536ae7fde3742944c059943c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5876de34cfee49629186985dc276dc8ff6d297cd83f167937fb26938ca7f4fa4`

```dockerfile
```

-	Layers:
	-	`sha256:071d046e5364f2b9f7b080159161c01c285ed9a2bccc73f60abfdd6a223985df`  
		Last Modified: Tue, 04 Mar 2025 21:57:02 GMT  
		Size: 2.8 MB (2827293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1455505cc2cdc87df3947b9885cbfe3a73347702dc11fbafeb4c424735da137d`  
		Last Modified: Tue, 04 Mar 2025 21:57:02 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-12-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bf8574f0c7d8be6fea179f52f6894ce561f9cc7a1e8fd7eb3d7090f385915004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239989011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dab391640bc32fd48928337b90f2133895c4b87096ce94793209b1f04b77d7f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d540a108360b4758f769d32386cc3bf9b4ba8ae7632f8a90567ce5ce4f3f98`  
		Last Modified: Tue, 04 Mar 2025 21:58:38 GMT  
		Size: 1.4 MB (1361271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c493aace335b3a898eae8adf5c89dd8b7e6561e9752f20a3e9bf411fccc664`  
		Last Modified: Tue, 04 Mar 2025 21:58:43 GMT  
		Size: 209.9 MB (209881753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-12-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c9b8dd5eee128dbce2d2328d66b144996ad92f472f9911a26f86c5002c67c102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c52a245834d4a5ea71bd914dd197c0519c688435ff8a49cfac552b6b38b1a3`

```dockerfile
```

-	Layers:
	-	`sha256:267606a29e8b13241b142ad223caa7069830adebe7b25941bc353d1ac20fb4e4`  
		Last Modified: Tue, 04 Mar 2025 21:58:38 GMT  
		Size: 2.8 MB (2826945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7781dd8916bdbba3b631fc60e07e6d389a09cfe7facbac00bf3288eba24f3a81`  
		Last Modified: Tue, 04 Mar 2025 21:58:38 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
