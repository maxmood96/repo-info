## `openjdk:25-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:807131104d66d7877ea936c15a0a4efc4768c7a906a569c61eb6937d049b5134
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:c62bffe9303932645f56afc3e46686dce9fe70722d1efb1fdb1b9c3c8abcb3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243472058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47c451d088c0d260362ea20a50d869f23a5bd651f0c956afb4b0a9fd0285f18`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb3d6be3cf652e24ce0966c0e22b427fd45e71af74190a8594d263bfdace382`  
		Last Modified: Wed, 22 Jan 2025 02:28:26 GMT  
		Size: 1.4 MB (1377236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ab5371200de7f9373031c67edbf3ac92f0b3cdcaf29d6fd82e1a4ebd0bf45b`  
		Last Modified: Wed, 22 Jan 2025 02:28:29 GMT  
		Size: 211.8 MB (211842157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:20ace5d18be03ca729a9054b537c2bdceeeac125b40d8883f9c6a7e00ed4a204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c40629a9691c5aedd87d13e17854d5bd0a3b90fdb94a7483db230a988e39abd`

```dockerfile
```

-	Layers:
	-	`sha256:b3b5a39602555946adfbcec074561bfb9a1d25995d40a4197750cb0973f75808`  
		Last Modified: Wed, 22 Jan 2025 02:28:26 GMT  
		Size: 2.8 MB (2827285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbe8391801c86cfcc1fe379c6ae7cf8da19e474f053da8abde466a42f3955be`  
		Last Modified: Wed, 22 Jan 2025 02:28:26 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2590810410a57c5cbe3238f9f48ae9b6bc2f4e476ceb7131da1f3e91e2a67479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239898737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a256d8f77de126856076f5caf2472618cba590654ede213354e42553e74de28`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696461101c67cc9af64403e8b92081fe283008fa12948c4ddab16982e126d03f`  
		Last Modified: Wed, 22 Jan 2025 02:34:05 GMT  
		Size: 1.4 MB (1361278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0e375dd100da0007910b4e6b9d28e4bc4886c9fc581b1e09bde62bcc8e0d7b`  
		Last Modified: Wed, 22 Jan 2025 02:34:10 GMT  
		Size: 209.8 MB (209792546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a2719649664360eaae05c7dcf0bed36021b3fa04c66eba17ea20b0ba67bf5fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c29794e8b8b5ad1d35c9261ab2992e73ee760be7e429bae9cdf90bfeba3043a`

```dockerfile
```

-	Layers:
	-	`sha256:2e5be5fd88a41c2fd21bc81c60dd935b510b3004843ebb965671d1ef5474fead`  
		Last Modified: Wed, 22 Jan 2025 02:34:05 GMT  
		Size: 2.8 MB (2826937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdeafabe74bb8b21d923acc700f4413c83023095234d9bab38286a0e31285aa4`  
		Last Modified: Wed, 22 Jan 2025 02:34:05 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
