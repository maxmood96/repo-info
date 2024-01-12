## `openjdk:22-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:1cc0b01d297970ca50dabca59812fdc4fe343c724d73c897be71be9d6a98d48f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:de21d40fd05f6cdb23ed0b29aac47b97dabc37c63a5c5c7e96ca68fd3892c4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235708845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f95a3c74447a6fbdd5567d44a7ce5f92bbf3d0244d08b1600ee958dfc76c46`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:48:12 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Sat, 06 Jan 2024 01:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_VERSION=22-ea+30
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='b0bc58519b965bba6505b882e5666c273ca5d2c192c44ecd5daba5efd3716ae9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e4c06460b2bf71e6f50fe574073f25d071bbde07323e02521fe6bcd7b9a4517'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1b7ef3d281dba8fd4b380a1adad23260ff86f27b60f2e99a4be020bd7664f5`  
		Last Modified: Fri, 12 Jan 2024 00:32:20 GMT  
		Size: 1.4 MB (1378117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de9cd92bcc85d2cc8f46fc9a6c6bb4b99baa9c15ef9d145654460b2347023b6`  
		Last Modified: Fri, 12 Jan 2024 00:32:24 GMT  
		Size: 202.9 MB (202912773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:09b49676c9230cb2a9f9d2fff5dd4496f79107020683f035e8a0a047cef9e746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c535be28d1fac437685aee4104222bf4920035871fa3be9c9c740c77b69832a`

```dockerfile
```

-	Layers:
	-	`sha256:5e7134c6481a0105bcacebac3dd649a5f6bf84547fd7f885c913ef0d9ad0fa05`  
		Last Modified: Fri, 12 Jan 2024 00:32:20 GMT  
		Size: 2.2 MB (2190189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ccf680545110b9f7b26e1feb9b30c14a08884175b217143489ab8a1a68ef3b`  
		Last Modified: Fri, 12 Jan 2024 00:32:20 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:74466bdb85dfcef8164f702c052715583f1da659f25b4436782a7a255979b595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232386652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d806baafdfe97c6f2297a388dc26b24dbaf265f5b7b9f29b2840ae941825af87`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Sat, 06 Jan 2024 01:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_VERSION=22-ea+30
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='b0bc58519b965bba6505b882e5666c273ca5d2c192c44ecd5daba5efd3716ae9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e4c06460b2bf71e6f50fe574073f25d071bbde07323e02521fe6bcd7b9a4517'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc02ea368438444f96ca14e22446135689f64999554dfd8cd20ab0b7c7a2913e`  
		Last Modified: Wed, 20 Dec 2023 10:24:06 GMT  
		Size: 1.4 MB (1361921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bfc1d7a7b2279367b707eee046c7750be8a166480dc78ceef5e79f97a82fa7`  
		Last Modified: Tue, 09 Jan 2024 02:28:22 GMT  
		Size: 201.0 MB (200960679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:de6fe82484e80e5c09a4d4b40aefa8260befc6335b3902227725dcff5f9e4b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893a5a2c4654334171b7a627c264ec48d5d7d2cef6a8adb2e7d2d54903cb8aa`

```dockerfile
```

-	Layers:
	-	`sha256:4124f7e9748f13467824b7b1dffc4ed6e3d310a75d2496544df1380c3af9ac0a`  
		Last Modified: Tue, 09 Jan 2024 02:28:16 GMT  
		Size: 2.2 MB (2189547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9e88e4a5799911ff9b03cc42b3490686be352f7c2ad0427ae2552b5c4f318a`  
		Last Modified: Tue, 09 Jan 2024 02:28:16 GMT  
		Size: 17.3 KB (17318 bytes)  
		MIME: application/vnd.in-toto+json
