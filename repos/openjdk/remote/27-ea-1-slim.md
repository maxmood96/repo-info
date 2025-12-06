## `openjdk:27-ea-1-slim`

```console
$ docker pull openjdk@sha256:a2b76c64c10fe8f2701c9384ccf376ad7210d31ac4b0f7039fa5f3a207fd77dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-1-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:37547c9f00cdeefaf78e93f9ff75ab1d3cc6eccaf1f216afed78f73464770273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260198258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb3604b8ebc9b287dc7a05bc6a58d564f9a16a53b5eba4c4c8b1659842d7292`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Sat, 06 Dec 2025 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 06 Dec 2025 00:35:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:58 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:58 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:35:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88d941ca811b52aef4354fe685363150d5ccee3bb7d4845ca197a5b3c078f47`  
		Last Modified: Sat, 06 Dec 2025 00:36:32 GMT  
		Size: 2.4 MB (2371013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676d93e84e919649d5ef1662c54d93862bcd0d74451cbda355c92232c28a3529`  
		Last Modified: Sat, 06 Dec 2025 00:38:06 GMT  
		Size: 228.1 MB (228050761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-1-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:968b787afd8ecbeabb7ccab7b5670c13d8a6fc9875b9b21a3341ad7a16780267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5e0b250eadd5ed17dd3b4bf6b6907cce7e2bd9da7b2449a804b5f7f1947a8a`

```dockerfile
```

-	Layers:
	-	`sha256:06d4aa9f15bfeadfed5e109c2d3d98ee3c4344f4640d2e51c4dbec28e0bc3337`  
		Last Modified: Sat, 06 Dec 2025 01:26:42 GMT  
		Size: 2.3 MB (2278773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863523378cd5cedc129ec3428738da49b17ffaa4674eb9c578bc17f3b84da910`  
		Last Modified: Sat, 06 Dec 2025 01:26:43 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-1-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:561ceda8f00f6ac36c31b9a8f566894fb77df4ae902662eb4414747f97031f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258416730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46df67c54eaf3dcb0f8ff512aa2546ae49c545d8dbdbb28ba47a762c9a921e4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Sat, 06 Dec 2025 00:35:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 06 Dec 2025 00:35:19 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:19 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:19 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:35:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee9e2063ee0f056c34e5d9359c188ba7ebd9066db58acd7f0a51fa63ca88e27`  
		Last Modified: Sat, 06 Dec 2025 00:35:56 GMT  
		Size: 2.3 MB (2314091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ebf7fcdf33c87df0d7dd6f85ebeea0c614e9a8591dc92fdfb16e00d1baf868`  
		Last Modified: Sat, 06 Dec 2025 00:36:13 GMT  
		Size: 226.0 MB (225964029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-1-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:b789350ded19c278a92d44be6180612ee8dac27576f0f5e4b68ae4f30dabbadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b082895d2d7ce5e8ba04b7ac4ff6b674c4b08fbb605021b4dd624dbe6440406`

```dockerfile
```

-	Layers:
	-	`sha256:faf6b3b9430f772d3ffc2896dadf3a92807a62959f4b0965d1c9921585a094e2`  
		Last Modified: Sat, 06 Dec 2025 01:26:46 GMT  
		Size: 2.3 MB (2278459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba8169faa136a96ee74e5467d8c87416b582e5be467e99146b3cc894eea5bbdc`  
		Last Modified: Sat, 06 Dec 2025 01:26:47 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
