## `openjdk:23-ea-13-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:34782c4b900012c4e7d264753a85d975ff51f7f1e00f911bb56a06d04f52e8dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-13-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c016e109cfc231a63a5164831004c2c14fe4bd66766d716f5b2f064fd4017996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236116674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5342191beaad36eba26aa0447eb8bbc3d2920086da14c97b9689ac432b70664`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 01:48:16 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72834852d1a4bbb4915610d9e1aa585fc13a5d3c47eef0c8586195f3548d78a`  
		Last Modified: Tue, 12 Mar 2024 01:55:34 GMT  
		Size: 4.0 MB (4014980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86d8c17beace3021d4ed72e254bbc0f764846472f9d3cde01e17ffad0a13fc`  
		Last Modified: Tue, 12 Mar 2024 01:55:37 GMT  
		Size: 203.0 MB (202977513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-13-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5ce897c833f3a510dc40f465d8a52daa60d24d481f1e1ead89e1e87381c577ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0277824c515c9e95c660824259ab429e0a1ac27ec3443614ce90b2ccba7f4663`

```dockerfile
```

-	Layers:
	-	`sha256:9acd17602fcfa7ef80497f120a229e5c8ffe4d4d9433763e6d4153a6f2873591`  
		Last Modified: Tue, 12 Mar 2024 01:55:34 GMT  
		Size: 2.3 MB (2347502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8024ddd39cc2afdb47113efc1853582a1f88ee5d368dd73bd374c275ed9fab67`  
		Last Modified: Tue, 12 Mar 2024 01:55:34 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-13-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:249ff7d59584a396a6cda4d199fcae72463ec2d1a9383ac1ba5b55b145f06b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233824775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d574fa5703c2bf8b1687a36fd2bc0536cb13738c85a7cda329eedbef4a100`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8410fe4fef0c872c792715fe6568a72fcb123e3a137f41f3bf25ccf0ab0780c`  
		Last Modified: Sat, 09 Mar 2024 03:59:27 GMT  
		Size: 3.8 MB (3820086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72805a05efa2b1635a27c2fe4914cd01b16406cc41a5cd44ae62196e8124f`  
		Last Modified: Sat, 09 Mar 2024 03:59:31 GMT  
		Size: 200.8 MB (200848326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-13-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a341c749298c67c813563547b2a474db01ccad7ff12e11b20fc3aa166efda457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83381f37b76af968e51c89326059da6238c423914b78bfad84d43772c0a4647`

```dockerfile
```

-	Layers:
	-	`sha256:a86d1165db938a4e7715591d8f416ff75b29495a47c989006ab63a81b10b45c3`  
		Last Modified: Sat, 09 Mar 2024 03:59:27 GMT  
		Size: 2.3 MB (2346772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c9aa7df9fb2ae70453515ca96aab62c9837eec9f4f14be237b457746b49b7f0`  
		Last Modified: Sat, 09 Mar 2024 03:59:27 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
