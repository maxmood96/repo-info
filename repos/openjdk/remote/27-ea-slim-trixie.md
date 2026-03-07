## `openjdk:27-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:88bfafb47f99a37335c704b67c7547a3c97afee6d7dbdebb360aee3462d82ca0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:7c9f8a0e0e7f5c7e4c0bd286adce5466e260eaa1c27255b4c2a9d9d322fa32e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260739346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa540727cd164982d2a2a4bff95312347e6b2200efa948feac52ac24f9487a7f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:41:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:41:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 07 Mar 2026 00:41:24 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:41:24 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:41:24 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:41:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:41:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663cac4a0baac0fbb8358eb45cd1e06da87e1b57812511ba2aca9a4dfa220932`  
		Last Modified: Sat, 07 Mar 2026 00:41:43 GMT  
		Size: 2.4 MB (2371001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85d8467992e124c2b7a45cfb0ba1f3e4cbebc9f7650b74181e64a2deb62ccd`  
		Last Modified: Sat, 07 Mar 2026 00:41:48 GMT  
		Size: 228.6 MB (228589713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4f6e26d79660e22312ce2307bacea9df347e57ac3003d6cb6164c9a2a919c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59178085d94385456e5151108000c14050ee8f6c5be273b048d8879445a3d071`

```dockerfile
```

-	Layers:
	-	`sha256:757e743d7715ebc3835adb743c31591e633218223324806d9a34a3a3ab49c4d8`  
		Last Modified: Sat, 07 Mar 2026 00:41:43 GMT  
		Size: 2.3 MB (2278859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a5257b0176f862edabe5b5f345e48dea67320554bac38faf693bfb442a904e`  
		Last Modified: Sat, 07 Mar 2026 00:41:43 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:27ffe7bc8a06db5b732c0151d606eb806dd4fa8a2ad5bc9467a160d1552214a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258990429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5e053cfce02344e354c7912a7e12b4551856107aae5d4af5b794e49be47387`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:42:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 07 Mar 2026 00:42:33 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:42:33 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:42:33 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:42:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:42:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6d916bdd4427c6032f65b8ddb1ed74419f14dbb4d5efbbd99518d1a2a8ebf`  
		Last Modified: Sat, 07 Mar 2026 00:42:53 GMT  
		Size: 2.3 MB (2314430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a2defc3261c4a927ac9123d301031f714e943db330414ada2229983ead0f9`  
		Last Modified: Sat, 07 Mar 2026 00:42:57 GMT  
		Size: 226.5 MB (226535901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0624a3e4ab2851694fc2c77e5ab8af6228d715097b7b057bc73eee765cb003f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851aa8ed7d68fbc0ebb1da890398f53181172145f2a7b9a06a362b93c1be4c41`

```dockerfile
```

-	Layers:
	-	`sha256:cb2a0891bc8182c9c8acdbac58289e4eebb814c710bd2950d571c31499794ab6`  
		Last Modified: Sat, 07 Mar 2026 00:42:53 GMT  
		Size: 2.3 MB (2278545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdbeec450d9e0dbff1736639324e8e0611f55dcb403d040642b6ac22793ecc09`  
		Last Modified: Sat, 07 Mar 2026 00:42:52 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
