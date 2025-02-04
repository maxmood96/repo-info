## `openjdk:25-ea-8-slim-bullseye`

```console
$ docker pull openjdk@sha256:a203d8cd0258ebd0ca3554b4a5d6b0e581a0debdfac688bce0bd047fecfd37c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-8-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:458f676a5addac33e901a858cd87b2bc4ed439c0002710e7acdd7a9d654de29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243559736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2bd640f9804afde9e33c3ac6fe3803b0cb476554832c1006fc22ec9e2cf69d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce4b8d6ba6b0ff59a273bca706ee114ed018ef3e89a057121d8c2b454ea6441`  
		Last Modified: Tue, 04 Feb 2025 04:43:27 GMT  
		Size: 1.4 MB (1377229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35908afe96ad209d3534491964e09f64bc2acf07b50a28de069ace291183aa17`  
		Last Modified: Tue, 04 Feb 2025 04:43:30 GMT  
		Size: 211.9 MB (211929919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a4f0deb8c2d92b66bf6e2b99fb69736a0c7b465cd7eaf93025549a7dd9abd758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e4096d1ce04bb236665b90f8f5174252d17afafa6fb3c6021370cca9086d1e`

```dockerfile
```

-	Layers:
	-	`sha256:5162b52d2825b25d2dcebde249f3460d0a5bbb6d08f07f3b0eeb4a0e2a20c69a`  
		Last Modified: Tue, 04 Feb 2025 04:43:27 GMT  
		Size: 2.8 MB (2827285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17948b323a5145ff824512d0f16c7ba0b0663fc8fb22c442b4bda6d08a162bee`  
		Last Modified: Tue, 04 Feb 2025 04:43:27 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-8-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:33bd788e603768cef471d10f7bd92f6950254fba93969d1e93f03d2a49c8a17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240006775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d773fc4f82cfcbaec0bfbd5d0dd2bed48290503008f16d49944d490c6a3c198f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ab3d281e75349c8d7e523dfe331e05eef1e55328ca9cf23395949e954a9cf4`  
		Last Modified: Tue, 04 Feb 2025 10:45:02 GMT  
		Size: 1.4 MB (1361266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66243a1b9b234dcea66a4ee7b5ede3a4e615e11135358b35a4f8b5fe3298118`  
		Last Modified: Tue, 04 Feb 2025 10:45:07 GMT  
		Size: 209.9 MB (209900699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3aa304174b0a760152a305a1cb0c54bca441487d1a22302fd1add3a96cde63f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b424e7bcc1b7a79fd34e11eeddce839b2da61a1cf29a7584751748bf7327bd`

```dockerfile
```

-	Layers:
	-	`sha256:7b59d3d0549dd67f7176e0278fb33c692038e0bcfd26e5ceba6dfc551a90376d`  
		Last Modified: Tue, 04 Feb 2025 10:45:02 GMT  
		Size: 2.8 MB (2826937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c1a5df9fab82f02ebf4318b62f1b90e130e20d3e2c1c31005554c5a7c7121af`  
		Last Modified: Tue, 04 Feb 2025 10:45:01 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
