## `openjdk:25-jdk-slim`

```console
$ docker pull openjdk@sha256:39563e25964d6b49c41d418245a505bbe50f3ca90b1997239f5435dd09add0b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:7b70ba9f17eb0e6e809668106f4c86f6cabd026ab727811717bcfc5f127b708f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244793373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daea03e231c556d401339f4c89e102b5fb1067e8782806804ba86b5c0cd2cfdb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f4f489846c1ddc55a76cad186a77d6c3a259340bf82c7d2d974efd40a035e8`  
		Last Modified: Fri, 18 Apr 2025 18:38:04 GMT  
		Size: 4.0 MB (4018377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fe6819c45e1557e232c002995674c6800e20ce4da0233df36b85aa08a3803b`  
		Last Modified: Fri, 18 Apr 2025 18:38:12 GMT  
		Size: 212.5 MB (212547737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:e71788ccebb4038be333f64fe5cfdaa2e8cdce24b53504daefcce20380ece873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a95616cc375ae909a13a2600544f0f7a4a8f97fad55d095146858111e0097a`

```dockerfile
```

-	Layers:
	-	`sha256:0fed2826736661b0a57d87581cc3021beb6b8610d9ffa661ddbb9c492f26cf90`  
		Last Modified: Fri, 18 Apr 2025 18:38:08 GMT  
		Size: 2.5 MB (2535252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f821c1aee0d9828bc18626401b348e45448c09b06fa73b7341c60863fda6c04d`  
		Last Modified: Fri, 18 Apr 2025 18:38:03 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9731c2710285298169e6608cf9962a8a2fdc112a284ce1a67b7466fbf87db7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242263535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52923b9e51729377d3d25ad0f662e891491dc6a937825e69f8d5f5177107cb69`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def4a1792f340f4e0e43ebb2cb541cdfe0533b6378c82fea5e9db4a63dc22d97`  
		Last Modified: Mon, 14 Apr 2025 23:01:57 GMT  
		Size: 3.8 MB (3833722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c53aabd5be047710054d2d91702b71e9e616cbf6217184356046b70c4edf8e`  
		Last Modified: Fri, 18 Apr 2025 18:40:05 GMT  
		Size: 210.4 MB (210363493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:e1bf5718e5c4748759a3d57601c3cef1554dc2a592ee6890cb505d6fa170437f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dfec92f51e25e68b71f8020c1af2c28045372880fc6e17bd48e0d30fb1dae6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4585360cadb86099c8372ee1164cd9c6f7b5fa4b74ff2bacd89b7700622fc3`  
		Last Modified: Fri, 18 Apr 2025 18:40:01 GMT  
		Size: 2.5 MB (2534982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c4b1f1736a2ab1d1367238d0bb2c7759ea3a2c1f27280c300ac1c720ee0245`  
		Last Modified: Fri, 18 Apr 2025 18:40:00 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
