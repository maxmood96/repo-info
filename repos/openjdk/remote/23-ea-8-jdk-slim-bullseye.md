## `openjdk:23-ea-8-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:21f87e076f104893579400fe2bf85afff8e053a8d4dc210bc279eeb6571a0dbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-8-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:b542cb18a9c1763089229a678fd95ab3dba672c61d28769864443aba933210ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236099216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6ca1fca7eeb757282be22d72d77f67826db2ad64f161e84a7041f55c93f0b2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f40d836cdc5e18b29d31457512ce76dc10119d7cf14bd0320ec32629c61aa58`  
		Last Modified: Fri, 02 Feb 2024 22:53:38 GMT  
		Size: 1.4 MB (1378085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be337dd925b818ff3e52cf0b1200accd08734bd9b6ec7e53f74bea32c5516a5d`  
		Last Modified: Fri, 02 Feb 2024 22:53:43 GMT  
		Size: 203.3 MB (203303304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-8-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:001f343b6652fc3c772cad1d8c77038c5bf7ce90388ed1e3370200e80e40ced3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4663268b63ac5293e1d2046b6c6bb2db1a17db258fe0cd5e01e4338240eb494`

```dockerfile
```

-	Layers:
	-	`sha256:d7061a11c81e029c37eeb865116e7d4f9eb656dd06f05a6d9aeac0e012833a6d`  
		Last Modified: Fri, 02 Feb 2024 22:53:38 GMT  
		Size: 2.2 MB (2190188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7558a81f79211d028cbef7b185ee3fc73f08f8e87b380ea3c339cb460f7feaf3`  
		Last Modified: Fri, 02 Feb 2024 22:53:38 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json
