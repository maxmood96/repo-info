## `openjdk:27-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:b1d94030ce24990b32d09a508eadc4150590a517ced55c9afaf32431fe72e15f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:95fbe9c632cd4f4bb1b2b12919a7cbafc5aba3ee2fde0e2a4cc8a586b0ee71ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260688021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ab98602d502400f3013324881a986818cb517c5130610ebf42ec599edc239f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 19:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:32:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 17 Feb 2026 19:32:27 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:32:27 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:32:27 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:32:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b0cd6d9ab9bd0291f4d0fd3217b0f94c014a5a5cf3bbd90fecec62bf49c2dc`  
		Last Modified: Tue, 17 Feb 2026 19:32:47 GMT  
		Size: 2.4 MB (2371031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6d303340c765c5c18b30473810f5d4534a1d662c57f6a23071b7366011125e`  
		Last Modified: Tue, 17 Feb 2026 19:32:57 GMT  
		Size: 228.5 MB (228538394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:63dd2ea6d6ced75eeb057b8673525e7ddcc3e84649776fb28a90173218cb3af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3215a830b1a32b183b16a7ced1e6c4178bd9b2ea8eb24242ed09ced2cdd64331`

```dockerfile
```

-	Layers:
	-	`sha256:d5c019b822579ed5b06565a2b095af2420a26bc632fecd1fb61c1fa96bc39de8`  
		Last Modified: Tue, 17 Feb 2026 19:32:47 GMT  
		Size: 2.3 MB (2278847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1429ad68659635420c30f8ed254714bd92cdb3bc9fe513f4a8e720fb3c86350e`  
		Last Modified: Tue, 17 Feb 2026 19:32:47 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:29a2f536a3702efff1615b5d1c1a174e208bbe30b0a2da920643662f2aaaf0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258939937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfe6fb028211456422fdde8854f3894792b479323170931a8030154182376c1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 19:31:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:31:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 17 Feb 2026 19:31:56 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:56 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:31:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12749f34a7eeafeaf309d7d09b09f1c60d585beab766385cb83dcb0b2bfc2b`  
		Last Modified: Tue, 17 Feb 2026 19:32:17 GMT  
		Size: 2.3 MB (2314393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816c3a1b93129354a0a432d1d15b9ff8a56ed53f01a1d89ea53b7c48ecd9e500`  
		Last Modified: Tue, 17 Feb 2026 19:32:21 GMT  
		Size: 226.5 MB (226485480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:dac5306029633715bda412cb9c44d944996101044cb752e0c830b7433ed0eb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16749740af0fe966db424c03741e6cada9c7ff0ec35e0906e7a5db31faa5f27`

```dockerfile
```

-	Layers:
	-	`sha256:2cb5a8f96deb70e66b36a93c2a28e702662a0806d40affb72b34775c497e86be`  
		Last Modified: Tue, 17 Feb 2026 19:32:17 GMT  
		Size: 2.3 MB (2278533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71f46ef549b2a6819430469d9be0a04947725083b06f55cc18cbc3f5035455d`  
		Last Modified: Tue, 17 Feb 2026 19:32:17 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
