## `openjdk:27-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:c0266c5308ccfe347c9a44a776b8c320ab5e0699026a5ac09bf2597b8203141a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a6454fd76600336c635f9b2c538a7cb57616850fe5a781c77f76a5d3fdd83044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259385802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e15b14807c784645cd088bf044e254f8060845c4daf306fd6d5e0f719848ce`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 09 Jun 2026 20:05:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:05:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Jun 2026 20:05:56 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:05:56 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:05:56 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:05:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:05:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5430a8c87537a3ee5982b242ad18cd439643930e8ff551cc0deb915b98b86857`  
		Last Modified: Tue, 09 Jun 2026 20:06:14 GMT  
		Size: 4.0 MB (4032608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd43b278aae3edf8f690632422ee3efd862acec78e90fa927b3e8dbcb1c42c5`  
		Last Modified: Tue, 09 Jun 2026 20:06:19 GMT  
		Size: 227.1 MB (227119651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:89e92468e208c88a4823195275d3adb54b03a626f1c5775e928fec17273dd0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f8005d51ad8ddc3b49ec05301bd8e36eb8e6e58d26deb196966026c795fa8b`

```dockerfile
```

-	Layers:
	-	`sha256:55f44fd34fdd25cd48b3d19e621a67d6b2cf19ee825b1d3e928e96579d89acd9`  
		Last Modified: Tue, 09 Jun 2026 20:06:14 GMT  
		Size: 2.6 MB (2647272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119fe505646d520511f35547413bc9ebb484927133faf5277372c0c1732c0e1e`  
		Last Modified: Tue, 09 Jun 2026 20:06:14 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1f63024f46b81fa31a3af841b5ee0172b83f2e9a454b40148f9d852c0cfa6594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257064371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e462809f4cedcee19e675b4216739d271fb803451ff096b35978166f7049b76d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 09 Jun 2026 20:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:05:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Jun 2026 20:05:45 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:05:45 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:05:45 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:05:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:05:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8828659408f8790a132d89293ad55b3d142101a26b89776d731e25104756cd`  
		Last Modified: Tue, 09 Jun 2026 20:06:06 GMT  
		Size: 3.9 MB (3852967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccebfd5e668705e292f7cdc5916ccb36bd694328c74088f15aee93c28b7a9d56`  
		Last Modified: Tue, 09 Jun 2026 20:06:11 GMT  
		Size: 225.1 MB (225096361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3eea6eae084e5e8cebb2508db99656464d24a750979c4e2da1d42e2b4b60dc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec33ebd12187a0d5b2334a746559d14cbdd90406b3303f325752e31e3239559`

```dockerfile
```

-	Layers:
	-	`sha256:19e1b3bc9a905221e41c5f62fdaf039d92e7587c627b99883ef98d1f267fd3d3`  
		Last Modified: Tue, 09 Jun 2026 20:06:06 GMT  
		Size: 2.6 MB (2646906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91754b54682c52ff05eacfcf81906cb7d3ca25e68b228dbfb856976ae9edb1dd`  
		Last Modified: Tue, 09 Jun 2026 20:06:05 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
