## `openjdk:27-ea-5-slim-bookworm`

```console
$ docker pull openjdk@sha256:6bae8537947847dbe8d01972761f63339359172256f56cce8959755f5b09066e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-5-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a715c1cff1d08cbb5d8b22a86054c3c061b2110d9db103d54255957b625c8244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260493901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f153717f0e3e2a0bb7f5728918ec38abf3b97d11dde76897205e8211265dd374`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 20 Jan 2026 18:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:46:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 20 Jan 2026 18:46:45 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:46:45 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:46:45 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:46:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:46:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7598eddde8ec1c5ef25f4a45d89108d27c4f85df9867f0968d81750d271ae51`  
		Last Modified: Tue, 20 Jan 2026 18:47:05 GMT  
		Size: 4.0 MB (4028172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e06fc128ba5a400c031fb33cec60bd6a70af58a3bfee20388f6dd8f8481e88`  
		Last Modified: Tue, 20 Jan 2026 18:47:10 GMT  
		Size: 228.2 MB (228237157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7a4b8e942aecbcfa7b1aaa995bc18a220f5bcb62d10c9f871517794a3e8c11c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2caf5199f7e723f873b5fbb08fd31b707d13eb593e1a4def2ed5a2d1ff58ec4`

```dockerfile
```

-	Layers:
	-	`sha256:657194ee85cb25e07e2b9ce7b11842a324d49361b93910da47b3a3ee41567e98`  
		Last Modified: Tue, 20 Jan 2026 19:26:27 GMT  
		Size: 2.6 MB (2649791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5da81272727dce7c3721ff5648a789daa03fe21ce05983680086a23b0553ca7`  
		Last Modified: Tue, 20 Jan 2026 19:26:28 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-5-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3fc1ea6c9940624480adcea838783ee1fbeb5d66261aae7129be4d4cd1e1f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258127868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e182b020971c6aaae10dded99b6679a0600bb5491f03eddf38373615d3dd4db4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 20 Jan 2026 18:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:47:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 20 Jan 2026 18:47:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:58 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:47:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1119870efa210bc214129b5837f82916a416d7e7080f89dbd5fecff367bf15`  
		Last Modified: Tue, 20 Jan 2026 18:48:29 GMT  
		Size: 3.9 MB (3851996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb868c271c997b9f8192eadd1576326e52dc24bb72e5f55a5ddad8bb4c27be5`  
		Last Modified: Tue, 20 Jan 2026 19:27:10 GMT  
		Size: 226.2 MB (226167983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:deedf0cb259d743eefbc0acff4f675d4aeddf816a450e6a194b430b31f75322f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45d71061e2e3969479d7e21ce34d61f3786f7041d641e3170859d3a07fa90a0`

```dockerfile
```

-	Layers:
	-	`sha256:a0d34bab6b4248657bff0c9e438f06f77a30e71c6e90c9874425ff98b8ec282c`  
		Last Modified: Tue, 20 Jan 2026 18:48:19 GMT  
		Size: 2.6 MB (2649425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:318cb3fc89c7f609312dc36cec2f6be07d02264f1a82fe232e73d98a4102808a`  
		Last Modified: Tue, 20 Jan 2026 19:26:33 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
