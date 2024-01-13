## `openjdk:22-slim-bullseye`

```console
$ docker pull openjdk@sha256:c046c9a9489c8e16e41be957686cca3cb68c71b61c04d2027a368ea2abbddaf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:7d87b1df5ae0933445464c9657fb2dfd3665eb6bc37b66b899a4e6fbc83ac193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235719098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab68c20d71baebac7d64eac20cb4e9406c9953dc42cff140fd33b93f6dda74c9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
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
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd9bfff6b30e18cf7b284bbc422e54ddd5598e6cde7e910bc17de055b9fd64b`  
		Last Modified: Sat, 13 Jan 2024 01:07:23 GMT  
		Size: 1.4 MB (1378129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6c972272bfffee3dfe845fca7acc026774ec8c3ef02bbb497bd922d401282d`  
		Last Modified: Sat, 13 Jan 2024 01:07:30 GMT  
		Size: 202.9 MB (202923014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3d6e4fde8e1f22d103da9b618ccf40e383ff772844ca2edc3041dd46ca7481b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137cca7d2e122b52a4e3b0c3be881ce8b94e98bd186c643638ca134e4e1deee7`

```dockerfile
```

-	Layers:
	-	`sha256:87c37588be02d84a0c4feb1e9b0c3dd5b4352e456142f2a61d2ebb3faafb6572`  
		Last Modified: Sat, 13 Jan 2024 01:07:23 GMT  
		Size: 2.2 MB (2190189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482b167b119e85e8f42e6b88fe6339c6ffe7ada8e7fbb2d387944bb1ca6bf634`  
		Last Modified: Sat, 13 Jan 2024 01:07:22 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-slim-bullseye` - linux; arm64 variant v8

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

### `openjdk:22-slim-bullseye` - unknown; unknown

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
