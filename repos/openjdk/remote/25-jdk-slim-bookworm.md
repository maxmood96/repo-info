## `openjdk:25-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:44864b6abc55c2f656ccc82bfe60e96d490023651b2b9468c9058bc840bbccaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d46510aebce16e41142ef6de396916d449fdc217d9222bcaae2435b258741fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255397451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193a07b569bde9d52299b8c6987f166f40c1f3ca9d67036fd7519c31d44dbd9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb34f81c0e54ea71495fa9d6649e70f978dfd886535f1a794f1babc06997d2e`  
		Last Modified: Mon, 09 Jun 2025 22:06:43 GMT  
		Size: 4.0 MB (4020009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fcbccf759d62f3b9cbc14a5bafa4b540d30560f71e645db90ac5593bd0886c`  
		Last Modified: Tue, 10 Jun 2025 00:42:24 GMT  
		Size: 223.2 MB (223152112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b23b8a8bbaced2d33a076462e9b8eaad962890a01c938793ce83d02cda68e412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4c0fcf91ea19f129c0302401600ea6de8e5c552fc76bfc37784b04c6655ef4`

```dockerfile
```

-	Layers:
	-	`sha256:94badbbe5b86f0ce7dfd1fcc6ad45059a6331226b28bef1e50cff04390fb5115`  
		Last Modified: Tue, 10 Jun 2025 00:24:09 GMT  
		Size: 2.7 MB (2651979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4174f527650bacffa3837f03fd1c4119657d60c48ce8a792966559a0564807`  
		Last Modified: Tue, 10 Jun 2025 00:24:09 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bdd4d4dbf03d3f37373084560aec38d3736e9600d73ce0315cdf47aaa17de55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252835517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00ad25b2b49e282b493ab6c54c577aec0f857783198c33e83e73b990e0243ea`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8146c9804947f80186d66b9250eee5d43b401e06d60a6f4b0867bfcea74b84e`  
		Last Modified: Tue, 03 Jun 2025 16:25:08 GMT  
		Size: 3.8 MB (3835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64426486eff02f7b68349b23e7c39e1e560589393f916b8a7a154be04a49a17`  
		Last Modified: Tue, 10 Jun 2025 01:51:15 GMT  
		Size: 220.9 MB (220934972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f9380e244f9a43a4e8c2f9f367f5b3e1bed59cfde4f6cfd22578d29b85dde27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7f9a6a140c2af8a1497e17beb0a55d24e864de3bc96f468bf0efd16992b9df`

```dockerfile
```

-	Layers:
	-	`sha256:a9a8a8fa705a52607d1877242a7949260f7762cc92b96df052efdcb1b0dda6b2`  
		Last Modified: Tue, 10 Jun 2025 00:24:14 GMT  
		Size: 2.7 MB (2651709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab31dffa77947ea0aef89d91546eb1e3029b65d23d8c0430e21deb14c8ef492a`  
		Last Modified: Tue, 10 Jun 2025 00:24:14 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
