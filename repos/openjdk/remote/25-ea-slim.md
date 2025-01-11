## `openjdk:25-ea-slim`

```console
$ docker pull openjdk@sha256:b435f2952b69622f042c279d9166b6f2148649f11b910c6da80e87545bc99e81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:4ebfdc94b0ea288f4a6e5e8748e56381baccd3f40d1b8a8c8a4d805e53790839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245133810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8d7b6256da01a7d9cc0fb7c3c11a526f07b4b69bd62756d0a5c5cb8a21257e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecf2ddb35d9a65179507f9e22f8a7f8910dca8990f58d51ab6206a108c8836b`  
		Last Modified: Sat, 11 Jan 2025 02:29:47 GMT  
		Size: 3.8 MB (3824698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692ec6ae91da9763a5bf4e1f5c5b6aa47125eb35459bd152dc58d2c62c28463e`  
		Last Modified: Sat, 11 Jan 2025 02:29:51 GMT  
		Size: 213.1 MB (213077531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ea750f37ab3ea6f6dff922051d4103def875340fa202128c5db63acbbc7f3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e2f802d1ee5cd0f651969357e48ce0d04eb1494f9158786d846e7882da9ee3`

```dockerfile
```

-	Layers:
	-	`sha256:b25d920aadbe302ae816922c43d9b2dfa764fabcab42770ca96ba918c890234f`  
		Last Modified: Sat, 11 Jan 2025 02:29:47 GMT  
		Size: 2.5 MB (2534507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80cc79229e8661161fe66b35d08ce09e8aea3381b2bc5ebe90f38bac4351a857`  
		Last Modified: Sat, 11 Jan 2025 02:29:47 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:aa7604548616a628fb4501167485c6fe8ec9e6bf7c53eba5cd59514782c8a567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242738754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61521491426d1d1fba1beb014b9bbb222182580340d6086f9eb603a5cefa90`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6ff135ed08a1ea8c79c626a6c19f1b6f682176f521b40dbddaa1bbe09b4fd9`  
		Last Modified: Sat, 11 Jan 2025 03:17:53 GMT  
		Size: 3.6 MB (3639390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304b097312a0407ddca82653564d6fe01d1924cb3497f13d0ed97d61ba483b17`  
		Last Modified: Sat, 11 Jan 2025 03:17:57 GMT  
		Size: 211.0 MB (211040641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:1cb3dc626a9895348935f7b8588c1179ac75f8037bc405d3415d062c40c01603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15c0d5da429e3bc0f6c49a2a2e92cd597546ecb657801cee30f4204be00f82d`

```dockerfile
```

-	Layers:
	-	`sha256:9b65274fef5630297990855c719963a55e68e4b4ae7195364e55c18fb31fc4eb`  
		Last Modified: Sat, 11 Jan 2025 03:17:53 GMT  
		Size: 2.5 MB (2534237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77aa5b7ad2cd3ba22f72f03da05bfecee957868ee409d5e07ed9cd97dc208b58`  
		Last Modified: Sat, 11 Jan 2025 03:17:53 GMT  
		Size: 19.6 KB (19640 bytes)  
		MIME: application/vnd.in-toto+json
