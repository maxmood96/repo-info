## `openjdk:22-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:7fa2d079958144fa1a22254c798cb25f41c0907f30cc81ce18d51358bb2ce809
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:2f22f287728906375b6c28c9af1fdc9334f848e41ed704904367b20d5789c1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235722693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc23cf39422f63e7ba362c374014837666a9f2f779a30aa72d586daa3862d94`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 23 Jan 2024 19:48:26 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 19:48:26 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_VERSION=22-ea+32
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='7ac0b8815f22c852796fa13b7680e07fa1dc340aa93f5e2bf1c5502337d952d6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='7c565754b2926817c1779683d6b8f1975a94a8731fad35a670ea669a77aea182'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d66926ec4547ed5c7ed370c7c145e4886458e7d8c318c1f1c9f42ea3fce979`  
		Last Modified: Wed, 24 Jan 2024 20:56:52 GMT  
		Size: 1.4 MB (1378048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbba5c731a9837d6ea88ba51ec75482dce312377799561e08d6455c55c610de`  
		Last Modified: Wed, 24 Jan 2024 20:56:55 GMT  
		Size: 202.9 MB (202926690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:276e7b6e146226b95c09b75c19133495c93ec39653568a475bf9dabdc6331b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52b563ac167d7d7339f8dfcc88d6129d1a56701e5bbfba0cb54d485a08e9acd`

```dockerfile
```

-	Layers:
	-	`sha256:6c8766cd630bac48a978921b3f59b329f557e5ffaa34db82655289c17612656b`  
		Last Modified: Wed, 24 Jan 2024 20:56:52 GMT  
		Size: 2.2 MB (2190189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e3090a002ca24d6d11597633990f6e2873549b18b49a2951884b8c62f3f6d90`  
		Last Modified: Wed, 24 Jan 2024 20:56:52 GMT  
		Size: 17.5 KB (17470 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f077916f768655623eaf7ca10582f1845b68f5b7d68e9603ebfa6a3a6ed79994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232405457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28512092ccb618e230a5233900305bd886e8b1620032ff8790868f2437fd9af5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864f90b8981b087545e440102e5efeb70861aaadc2193e6caa6a685b8ddd18f2`  
		Last Modified: Fri, 12 Jan 2024 09:23:32 GMT  
		Size: 1.4 MB (1361926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c75b13bf0dc52c22ccd0e0fdc96eb8bbaa4801d2052f253a26e97e26bb86421`  
		Last Modified: Sat, 13 Jan 2024 01:47:44 GMT  
		Size: 201.0 MB (200979521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:18572caa7aebe4e6eb0010fa3da0552a86a4457021824542de51918e8e9aa151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d261c7e073c42c178da167d79eff5041c5303e77e009b86f27a320143a04d4`

```dockerfile
```

-	Layers:
	-	`sha256:2d806a01599de5bd2a4610328e9cd3113efdd296a9fd44cded2b938320ea58a7`  
		Last Modified: Sat, 13 Jan 2024 01:47:39 GMT  
		Size: 2.2 MB (2189547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78d7323b9daa1df52f1f6bef8aa66fae8a31ea0d41f5844da610fd9029cb0ac`  
		Last Modified: Sat, 13 Jan 2024 01:47:39 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json
