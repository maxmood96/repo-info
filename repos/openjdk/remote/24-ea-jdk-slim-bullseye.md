## `openjdk:24-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:6c5e75cdd322e2ae4e0f1ca314d28ff6d67ad5b23a5c0c0b9e5b1d510b017940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3eef72d57350d09b7f2b58f63e87483d5abc1db6a28b3c93cd5f0e1b479e8ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244535171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187978d8bb8530645c1c6a6fed0e4e93a8bce1aed0d0e0b0bc3917cb27b40730`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6447b3bcb950c338dcccf3b6c41c179de724d245d123d288e5e52083761712`  
		Last Modified: Sat, 14 Dec 2024 00:30:12 GMT  
		Size: 1.4 MB (1377281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c13d8ca3b6d6829975d30bb0cfa9fa73d3a7a3db32a842d6d0273486200e4`  
		Last Modified: Sat, 14 Dec 2024 00:30:18 GMT  
		Size: 212.9 MB (212905246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:83a8863f9841af7f75a6e8edc0b16684b87228808df0f3e024b0fe5f433e1888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e6b5101233436bed42fe292b8653951aa55e4620048b546e8f29771908f1d3`

```dockerfile
```

-	Layers:
	-	`sha256:e25509b34251b474f65bb9ee34c85064c3dca38ff0ac7d111071ce4fbdf839a1`  
		Last Modified: Sat, 14 Dec 2024 00:30:12 GMT  
		Size: 2.8 MB (2830879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86cb057f970f77377e408e680de4a7bfa192951f76ea24a1786d72f2668cf924`  
		Last Modified: Sat, 14 Dec 2024 00:30:12 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c510c898b6f898a281f614114d5d6feca627aa834aa87f75447ac12153551657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240974440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c30e8634478e4268dfc7449ab9851728de14262ced9a86f23bd709597a76e2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7ad6e84f249b4b319e4c8cf12e7929732105f68e6f8a67945acfd605733bd`  
		Last Modified: Tue, 10 Dec 2024 01:31:31 GMT  
		Size: 1.4 MB (1361283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89567b91721d96e6e97e26f3b42683ebe68ac14ee64b6250d461f473fcf68c`  
		Last Modified: Sat, 14 Dec 2024 00:39:33 GMT  
		Size: 210.9 MB (210868234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:73d787836c7f7c4115277327eb3aaefcbef5d27359d9485cbd7b7f5cd2cd9524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebcacfb506495fc72fe0390d12a66f2d04e3e820120697008f11ea4c7f1b016`

```dockerfile
```

-	Layers:
	-	`sha256:866cc98f6595d20e7e2e21befb7877d45a25417508b3fde45144fb05f320e842`  
		Last Modified: Sat, 14 Dec 2024 00:39:29 GMT  
		Size: 2.8 MB (2830529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:251b9f4473aabaa9da3d669ce248e290c4f7dcc3060c95f21d1d030d35767956`  
		Last Modified: Sat, 14 Dec 2024 00:39:28 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
