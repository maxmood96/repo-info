## `openjdk:25-ea-11-jdk-slim`

```console
$ docker pull openjdk@sha256:9a65ce8af60e1ad9d5c107f847e0926399f746251c825783b19819ee819f3b71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-11-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:f96d385b279b144bfd6b95d3f3ba8a61b2e6afc535c6ed5e93ef341677e79416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244220024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71c26067e1a47553601f883624327ed583ad59a001fc839cdf1254eb3efff25`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Feb 2025 01:48:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d59d1b6ad55195c43a0f695ba055fba063a7502cbc2b54d54be7bd295de356`  
		Last Modified: Tue, 25 Feb 2025 02:28:40 GMT  
		Size: 4.0 MB (4018454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bbedab3e95a282b4561892d8affa2d37ec4adbdbc7efca97edf100814132e4`  
		Last Modified: Tue, 25 Feb 2025 02:28:45 GMT  
		Size: 212.0 MB (211982269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-11-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:116b7fbc5477877a70b68178ad505c0fa26d7679fb788b3fadb25f445ccecb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2557109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c9249541d3af387d48377534eb04c512580af16bd8f2b2b1948ccba8c6037c`

```dockerfile
```

-	Layers:
	-	`sha256:d41d99d70aed2844aeb1f2ea9a51cc79b7959fb6c18c57ce9fdc1d41ae741e7d`  
		Last Modified: Tue, 25 Feb 2025 02:28:40 GMT  
		Size: 2.5 MB (2537668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c70293839fcd57a8acbb0ec1a13f92d8f6b70da302e81d0b7e9f0bbc0485d3c`  
		Last Modified: Tue, 25 Feb 2025 02:28:39 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-11-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:49101377efd1661592abb606114a82f0454e9cc77b594c9fb44993254d291408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241821014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56e68512aca2ab79dab526d0aebb0d955fc4678384f684a7855a204e095eec3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Feb 2025 01:48:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03836795e052bd204c97153d3a2eae376a6e2ded0d4c7d40ee711d03630b582`  
		Last Modified: Tue, 25 Feb 2025 06:26:00 GMT  
		Size: 3.8 MB (3833744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3faabc0370fd245b39c5eea97e654a63ad8f0f516a6f6c68e8dc9b39cad31a6`  
		Last Modified: Tue, 25 Feb 2025 06:26:05 GMT  
		Size: 209.9 MB (209938845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-11-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:d1609918ce5b5cfa3890843345ba1e97eb1a0c65b0c878937cffa9c7dfebf38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2557054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad52382a0cb2c107cc512ecc40efc41f2a2155288e44c900430e1683ff6f6b5`

```dockerfile
```

-	Layers:
	-	`sha256:ac606d49786edb351832689f4aecf10593298fb4e08197bc2fe5e0d3bc4aa350`  
		Last Modified: Tue, 25 Feb 2025 06:26:00 GMT  
		Size: 2.5 MB (2537398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb07bbdb5aa0998d3f5a9bdf59490a97e14e9a13f014be934337f158bc30d089`  
		Last Modified: Tue, 25 Feb 2025 06:25:59 GMT  
		Size: 19.7 KB (19656 bytes)  
		MIME: application/vnd.in-toto+json
