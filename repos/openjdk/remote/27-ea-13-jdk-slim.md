## `openjdk:27-ea-13-jdk-slim`

```console
$ docker pull openjdk@sha256:7929ab3b113180b90fc114e9c32e9b72b172a37410a5244308d9f311d8e2c392
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-13-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:17cd55199209c64f36214be99363c301b814371cd7f2d5b22fdf2160124673fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263719128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aeb061da8a2d8ebe9cc3c0ac3a7020080ea8d0957c8c979efd9fb415626464`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 16 Mar 2026 17:03:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 17:03:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 16 Mar 2026 17:03:51 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 17:03:51 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 17:03:51 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:03:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 17:03:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efedecceb583b242d17f43bd87e2960c40a4f063ca5895e9544beb0632374951`  
		Last Modified: Mon, 16 Mar 2026 17:04:12 GMT  
		Size: 5.3 MB (5333751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bad7d797352b5f5deea823720e031f367e08b7aa6c4ae826dcf0e4b0f92e2a`  
		Last Modified: Mon, 16 Mar 2026 17:04:17 GMT  
		Size: 228.6 MB (228606745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:9578f801460c6d4fabcc261512736a53e914f0212a247294154ab0fc9b100610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a967a9c1f5de84fe483fcf5e46552ca21ad909502900b6b576b80d38d16524a`

```dockerfile
```

-	Layers:
	-	`sha256:3087be8feced49e23440ebb75379d71d6f24b6d032efe56464902a9da5d28841`  
		Last Modified: Mon, 16 Mar 2026 17:04:12 GMT  
		Size: 2.3 MB (2278859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af2bdd212aa7faa47de3e06af923cca3b188568dcee69a2f56d7ecf5df6e328`  
		Last Modified: Mon, 16 Mar 2026 17:04:12 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-13-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:39c3c09dc2a008b894184ad9b2bf57be6ac9d5678a5503693777c9bb9af7f941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262351631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f0f5e57ea2a251f56841eec27caf9a5465135340ef8dd69faa15d6fe14fbae`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 16 Mar 2026 17:04:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 17:04:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 16 Mar 2026 17:04:27 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 17:04:27 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 17:04:27 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:04:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 17:04:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3f9f087a773e83c5247746926bf70200dc39103ca8240400b46510c95ec4d7`  
		Last Modified: Mon, 16 Mar 2026 17:04:47 GMT  
		Size: 5.6 MB (5639178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c333a5913cbb7972b89c6a4f60e21f60e760ee9d65da31db2a60ce092f9c0e`  
		Last Modified: Mon, 16 Mar 2026 17:04:52 GMT  
		Size: 226.6 MB (226572355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:72dc70a82d9dfa16c42d935543a4b192c23fe3c34cbd0809c8c5e3be5588acc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176d15a1e52cc27d56d25f1eca2506241d15e0a9cf09877bfbd20de761e8a463`

```dockerfile
```

-	Layers:
	-	`sha256:590e922b76f042edf1398f6494192f1fa1f60ec1c8392049226c33ff4e285403`  
		Last Modified: Mon, 16 Mar 2026 17:04:47 GMT  
		Size: 2.3 MB (2278545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e14b8815dd6eef49267bb9ec1b7512e3e0ad8f9c74b8acdc9b3bb5953634117`  
		Last Modified: Mon, 16 Mar 2026 17:04:47 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
