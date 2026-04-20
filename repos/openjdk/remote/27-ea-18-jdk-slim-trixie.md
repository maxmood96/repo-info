## `openjdk:27-ea-18-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:776864db234c11dc6bf2ab8cb1a58fbef657e2a94ec1bafc37ad397e77e4fbd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-18-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:ad432242783a31896b570c3dbcc00ffc714b6a3040e9b4842608e49cfe74c3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263898787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff683ad0dc3c42ae54d1bb4fc56bdc13b58e906036baab544f35fe963a501d55`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Mon, 20 Apr 2026 17:41:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 20 Apr 2026 17:41:37 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:37 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 17:41:37 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:41:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Apr 2026 17:41:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75daae731cf5fcef24d8053865ab032b6d4eb1093d0274aba1d48df5faeb11a`  
		Last Modified: Mon, 20 Apr 2026 17:41:57 GMT  
		Size: 5.3 MB (5333962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0e553de17ed82b03feba2fb02163e06430c0205dfb4b86e6d76cf4b2ffe936`  
		Last Modified: Mon, 20 Apr 2026 17:42:02 GMT  
		Size: 228.8 MB (228789185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:c5b74d2acf5688e44fb6404d27b77b7edca7da252024c6e675404c015fe9d83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c5b798217eec9e77c3fa1f649cf31e12020402883b482a52277575af6ff0a0`

```dockerfile
```

-	Layers:
	-	`sha256:40a35292e7a80560780c3fc9e310330497d1f966336516897c6dcb2357be0a75`  
		Last Modified: Mon, 20 Apr 2026 17:41:57 GMT  
		Size: 2.3 MB (2277625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5af23c966de9afa01c4c1a2e06d4301d24f79554ea12924080a815a980851d`  
		Last Modified: Mon, 20 Apr 2026 17:41:57 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-18-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b12311ac86a5f064345c239b0083b840b4e8a25a54cf39b74ac294e3dd3da1e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262527580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed6ef29a973711b36b83b6c9e5bac38f86492a4543511c8867a15cfc990a83d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Mon, 20 Apr 2026 17:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 20 Apr 2026 17:41:25 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:25 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 17:41:25 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:41:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Apr 2026 17:41:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775d5fc89dc8dd2a1fed44f4b914418d2272d27b130ff567c8820f0047c4e333`  
		Last Modified: Mon, 20 Apr 2026 17:41:46 GMT  
		Size: 5.6 MB (5639521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2689826048fcf20394ccf806e1e795004224e34462cc29734f1c73c97bfe27`  
		Last Modified: Mon, 20 Apr 2026 17:41:50 GMT  
		Size: 226.7 MB (226749508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d2ab083582a55db6c350145e7ee4a9aaeb903b19996f91f3c0ec634ddf59cfbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea236292aaff58e583b7eadea151aa0cbef1d56127366568608aa563da5682f5`

```dockerfile
```

-	Layers:
	-	`sha256:9545011c41c5a214f7a440a3862507055e41989dfc49dbfc964b28147d4f7403`  
		Last Modified: Mon, 20 Apr 2026 17:41:46 GMT  
		Size: 2.3 MB (2277311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad383bc294d08500c690714766e7d953be3754b52271e19ec060cc44f70c043`  
		Last Modified: Mon, 20 Apr 2026 17:41:45 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
