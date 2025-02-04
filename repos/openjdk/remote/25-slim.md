## `openjdk:25-slim`

```console
$ docker pull openjdk@sha256:68109b15048b111d70fa71f6fc2afbf1981a3541d551df1d87b3cdece53c96ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:c07be4a76758307e8d5a9323e11b01e4008a3b1a89d83a1cce47ecc65498c923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244165683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413481b2d4de13b23dac435d813f4e664417df0f55789f1629d403f8749b37be`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b1e970d9b2de95b50b2a9ecc79b2ed452ff9145266e6ea0c98d435c71830d1`  
		Last Modified: Tue, 04 Feb 2025 04:43:36 GMT  
		Size: 4.0 MB (4018418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2094e13cf988b8ee71c97abcc9207dcd6862a0af95e10fe97120b7f48f8248`  
		Last Modified: Tue, 04 Feb 2025 04:43:40 GMT  
		Size: 211.9 MB (211934962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:5fdd8cbdc8c91f49e961ec2d47710d0b7e3cc2b85d4a2bacfd8d52ee98ce182a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff4f10b7f2b45563be9686f0872620a56acbeb29898a2dba8347c2c1c4b0876`

```dockerfile
```

-	Layers:
	-	`sha256:dc025a3786d35a9c57868d4918cd2b751dbd4722cbd6e0155ff0ed05ff8c41b3`  
		Last Modified: Tue, 04 Feb 2025 04:43:37 GMT  
		Size: 2.5 MB (2533878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db58887d814db4c20dd095cf81507ef432080dc7c845de26e7228cdded04822`  
		Last Modified: Tue, 04 Feb 2025 04:43:36 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:23e960b41c7fd0c6aea5325fd7f3a356ea0527f363203dddb644731b0f4b2d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241780025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf4036c08a04e8caf444f6a2bcfc15567ffecdc9b9c162e5d261a3f7af3a1d3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581a00b5a05c96a59ee2d9151f24d1e5a8071c04d7471e01bb3cda14fc06c99c`  
		Last Modified: Tue, 04 Feb 2025 10:44:12 GMT  
		Size: 3.8 MB (3833711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2aa022940de7d7da3d4e53eb711d75fec96470a127a71ac6c4c638da14c9aa`  
		Last Modified: Tue, 04 Feb 2025 10:44:16 GMT  
		Size: 209.9 MB (209905433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:ad919983a18b6b64e33d3db333ca2a910600c8d1b2615e02af74046dff0d4f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a98be12158b86daaa104c5899d09eee1c22a995505cc69885ac92c078e2a4cb`

```dockerfile
```

-	Layers:
	-	`sha256:87948da37419c3a7a82cae801c176d8f67d898541b83ed90d822569a47790f89`  
		Last Modified: Tue, 04 Feb 2025 10:44:12 GMT  
		Size: 2.5 MB (2533608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fb465e0335e038f057a2b67f96ba1b9446faaa4acc79fc112361061eb460f85`  
		Last Modified: Tue, 04 Feb 2025 10:44:11 GMT  
		Size: 19.6 KB (19640 bytes)  
		MIME: application/vnd.in-toto+json
