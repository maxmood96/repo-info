## `openjdk:20-slim-buster`

```console
$ docker pull openjdk@sha256:329a6b578d29100d33ec5fa893cb48a4a82697621bee499dbd21c158110c73e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:4dfd6774e90d32a6105e7c291dd4a59e8947be30efb1f1b9442672ef6cfe1a42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227913164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96426ecdd88c6bfbcf147e9afdeee1769299c670bb34719298e4f45c17779f68`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:29:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:29:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 25 Oct 2022 04:29:04 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 04:29:04 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:29:04 GMT
ENV JAVA_VERSION=20-ea+20
# Tue, 25 Oct 2022 04:29:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='0cb0f79bee2e61134a86049952a1e572bb3e2dad49aa200a20f18c697715a402'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4db7319dfbfb4a3561e9707c0178d0ba8d6413bc94f13d8c9ce406fd7445e000'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 25 Oct 2022 04:29:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04045c4766379cb0b4fc93bb96707506245d8d2e952cc00e74925a3994f6ec34`  
		Last Modified: Tue, 25 Oct 2022 04:33:18 GMT  
		Size: 3.3 MB (3275908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c566982ff64d822f4f6355b307d46f0feb290e8db8cc7abd27baffe9fd76c19`  
		Last Modified: Tue, 25 Oct 2022 04:33:32 GMT  
		Size: 197.5 MB (197496424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f4a89a1fe641852016510b3a56301adaf809eab999bd956a951b914a9a0f456b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225103742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf3bea7f2186aab3d02622c6c2fe7794acfe9a7b190a8eecfd135e684fba78e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 00:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:45:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 26 Oct 2022 00:45:37 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 00:45:37 GMT
ENV LANG=C.UTF-8
# Wed, 26 Oct 2022 00:45:37 GMT
ENV JAVA_VERSION=20-ea+20
# Wed, 26 Oct 2022 00:45:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='0cb0f79bee2e61134a86049952a1e572bb3e2dad49aa200a20f18c697715a402'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4db7319dfbfb4a3561e9707c0178d0ba8d6413bc94f13d8c9ce406fd7445e000'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Oct 2022 00:45:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13616a3846ecd154918e95271126bfcebd73bd0090135c17f7836596878e708`  
		Last Modified: Wed, 26 Oct 2022 00:53:01 GMT  
		Size: 3.1 MB (3129308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94439d8d1aa3608dafa231a9be47b5a4fb331ff47842339515523b451c0b07e3`  
		Last Modified: Wed, 26 Oct 2022 00:53:13 GMT  
		Size: 196.1 MB (196059549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
