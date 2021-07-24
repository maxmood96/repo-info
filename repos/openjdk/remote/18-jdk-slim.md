## `openjdk:18-jdk-slim`

```console
$ docker pull openjdk@sha256:773d28b324dfb1df93114d9dbd33bbf60d72dc0b2fb80ab8b77eeba79dd428ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:622e5898b2f3dd6eb0dfe3933e43b3a88f70d2e6f46c6bbb544ac22739d98834
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218327094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718c9d3c0ae06d9132673a82aefd434d61a4788e482c1ee40c495f26fe8df77e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:33:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 22 Jul 2021 13:33:35 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 13:33:36 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 21:21:18 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:21:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='03f895bdf47691e44e9b269eda74f407715e97385b0cfb60304bcfda29f589a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='bc3dec6f82541afbd83e9b5ba6ae70541206accd7d815dd171fd36c93a90fe3d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 21:21:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d5ef013a6164e3b6c391252d0a26dbd18a3c564f734d771b4033a83f6d84a9`  
		Last Modified: Thu, 22 Jul 2021 13:43:45 GMT  
		Size: 3.3 MB (3268756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e834d16d44c1b1b4b37ce26800f857ac6bac0d596cdff6fa400805a39da23b`  
		Last Modified: Fri, 23 Jul 2021 21:28:31 GMT  
		Size: 187.9 MB (187912543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b4330eab273dcc5c2dd9b0e0f6a688ad19389f997733ec351c01cb2ae8bf4a17
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215691355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3da44d50a2b21b37f9f3e536da7be4b325496db7de5749518f68a722aec464a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 05:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 05:15:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 22 Jul 2021 05:15:47 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 05:15:47 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 21:41:44 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:41:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='03f895bdf47691e44e9b269eda74f407715e97385b0cfb60304bcfda29f589a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='bc3dec6f82541afbd83e9b5ba6ae70541206accd7d815dd171fd36c93a90fe3d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 21:41:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e464611cad28e3191fb5458b5b6b9bbcfd879d9863a4aa29debea8bf188cc100`  
		Last Modified: Thu, 22 Jul 2021 05:30:12 GMT  
		Size: 3.1 MB (3118880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12625ffb33a426bed8c98265cf1ae45031f5c62670766091bd126702c8a790c`  
		Last Modified: Fri, 23 Jul 2021 21:54:31 GMT  
		Size: 186.7 MB (186657681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
