## `openjdk:28-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:03dec84c1a6cc22a6a2093107c5035b461fc8634bece6b25cd07579bf0bfd49b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e1cb96ab5e603dc36ddfe86cfed46215e63b883076d714aa78adf8832a360a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259849131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd31e48b471ac536255e91fa43969e3f197933d5f732f8852a0f59c7caf18b8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Fri, 26 Jun 2026 17:49:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:50:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Fri, 26 Jun 2026 17:50:03 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:50:03 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:50:03 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:50:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:50:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c957126c5533f1ade49a22837b7323e489aeaf30b26ad91c8ea30e53f628fe97`  
		Last Modified: Fri, 26 Jun 2026 17:50:23 GMT  
		Size: 4.0 MB (4032954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85007d50c775a9ecdd0a271b8a7ecbe74c41a0fc8bbf46f0a8837046442daa3`  
		Last Modified: Fri, 26 Jun 2026 17:50:28 GMT  
		Size: 227.6 MB (227578538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:81eb0eccea8cf9067eb2814ae207980d7b6398efbd056981b4ab4933c9a5d7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2303524beb4d1ab2eae0ede55c945e3d3838b54deeebd2489a8381964804df`

```dockerfile
```

-	Layers:
	-	`sha256:ed9409d451c5cbf543d082414ced962a926e04e368ae7779c135167439b9cd35`  
		Last Modified: Fri, 26 Jun 2026 17:50:23 GMT  
		Size: 2.6 MB (2647282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8601988c5d6f4a830e9f95c5f57f320e7b4ad2c5e7c165da4f906aded83bda85`  
		Last Modified: Fri, 26 Jun 2026 17:50:23 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:29ccbb8ca7b71e055a89aef45852441c5dba22bbc8996e18e305b83456f431d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257595853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7bc3d8eabf6f0e44354ec6a8eb5949a0d6b492c1f75265c70a1ec28b8b9062`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Fri, 26 Jun 2026 17:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:54:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Fri, 26 Jun 2026 17:54:53 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:53 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:53 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:54:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f63e096ffd29d524ca27f5b7bfe01ac646753d2c24c3971161fdb82df406e83`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 3.9 MB (3852830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72236bd5dd500c856c5f6d7a67cb6948871e9dc12afdecb6178fd02576b5b307`  
		Last Modified: Fri, 26 Jun 2026 17:55:20 GMT  
		Size: 225.6 MB (225620605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c9ebd03c616bc6e03b68f0bc2bb9db09daa495ae5bc8be1d78b19b1f0f92221d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c533914dd03f21bcc247e1c05e7a115b25b83ad08e97fe8c7ae54f2b312d024`

```dockerfile
```

-	Layers:
	-	`sha256:f29fcdd17bfbb5c525c03151bec58a3bb4d1adc071e40d52aba3cc6ba1cb825a`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 2.6 MB (2646916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f54396712c5843e172bd6d60d6977e8108316a7a47c499bc9d8f436bf1423a1`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
