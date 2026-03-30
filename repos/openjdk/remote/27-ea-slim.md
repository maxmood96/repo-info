## `openjdk:27-ea-slim`

```console
$ docker pull openjdk@sha256:bcab66071a2ff3c02a657a42d652a84d1a1809390b1ab5b1ff7637c9f97b193c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:593b8be6e84764a0f0c424063f5bab03b5cc4eb591b3b8d81d73c74017e11af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260805564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c41501faad76f890ec93819ce5f870ae78887b19be7fc61023121a80d1847a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 30 Mar 2026 17:52:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:52:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 30 Mar 2026 17:52:49 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:52:49 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:52:49 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:52:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:52:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b49b8fef7671acf9b6002ca1761ba44aad03abe40f3a3a5c397c9434778b9b3`  
		Last Modified: Mon, 30 Mar 2026 17:53:09 GMT  
		Size: 2.4 MB (2371117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c7db67944e5cf9e52801776dd71f4d23f244c626a8f4e1cde071563a0d36f2`  
		Last Modified: Mon, 30 Mar 2026 17:53:14 GMT  
		Size: 228.7 MB (228658947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:ca35bf3488b110a6a968252b6018a08520bfb256a3d24b68e0ad27dfdc5e6a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0998ed4f592ebc54d1f2d21fabf24b05c6e79ebaa64f03caebe998d9a1f6a`

```dockerfile
```

-	Layers:
	-	`sha256:d3568b14a2b26b24c84b8eacb2cdf47291792e35ec1fc2479005f8533b746610`  
		Last Modified: Mon, 30 Mar 2026 17:53:09 GMT  
		Size: 2.3 MB (2278895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccf48e89a75976fc866d9542f1c3e2266a4c3d8301185af1266104cb8e33889`  
		Last Modified: Mon, 30 Mar 2026 17:53:08 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f438681bc5127571877ed8f6b7a3d237238913a077432a8467616cba4090a467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259075767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831e7d85d0fc52189fbef7b1893e71a6cde6ef65771f84a3527c43992735f26a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 30 Mar 2026 17:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 30 Mar 2026 17:49:45 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:45 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:49:45 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:49:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:49:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e387fd19c06945fa8bdec7435245a960e8aa36860dcddb3c60da5ca088948e3`  
		Last Modified: Mon, 30 Mar 2026 17:50:07 GMT  
		Size: 2.3 MB (2314413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ea6c0c915d13b9a514e1c7f2b8351be52152da5f2fbd51c8d712447211e13b`  
		Last Modified: Mon, 30 Mar 2026 17:50:12 GMT  
		Size: 226.6 MB (226622938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:249ef1a05cf92dc637e3f58a5723b0c0ffc1798a91289d48532302e16d3a7f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c76f50e03e2e6373bb96f6de1bc9eb595366eb660532b2ca51c7895b328fc95`

```dockerfile
```

-	Layers:
	-	`sha256:b94bf59db96eac85808c69829e8ddfc142682a33259dea27be5d5c8f6109d3b9`  
		Last Modified: Mon, 30 Mar 2026 17:50:07 GMT  
		Size: 2.3 MB (2278581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbce5642a1c976d19c595eb6908bce42ae0dc1bc641ce37808e82fda4c12d1e`  
		Last Modified: Mon, 30 Mar 2026 17:50:07 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
