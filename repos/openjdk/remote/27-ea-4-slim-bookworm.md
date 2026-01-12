## `openjdk:27-ea-4-slim-bookworm`

```console
$ docker pull openjdk@sha256:0839206f0ccaf58ce93a28e68533dd8e5065016f8f062b2d1121345e4663a629
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-4-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e4f4aaf2feb528de8502fd4e9fddcca215a54c88d696e2e7e0aec658d09463bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260341536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d0578a02509e4f4c2281d357e7da067fbc2a4cbdc1c267b807c9e8a2364c0a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 12 Jan 2026 20:08:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 12 Jan 2026 20:08:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:41 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:41 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:08:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cedbca6c73c34966a74d6c7215c3c4e1fdb7b5d4f4182dcf4eddce2741aa1a`  
		Last Modified: Mon, 12 Jan 2026 20:09:12 GMT  
		Size: 4.0 MB (4028126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c0631255494adf6bd81a3c23467be6635096e0ec51201b99a58458f414c596`  
		Last Modified: Mon, 12 Jan 2026 20:09:18 GMT  
		Size: 228.1 MB (228084986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bdcf932564ab845dda712dd3be21a89b69f52aca7b0b7899ac1e84a968db1bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb72606d893534e71d608feb5d044eae8b8c1e55bbc8658e644ee2325ce4bda6`

```dockerfile
```

-	Layers:
	-	`sha256:c6b618dbcb71b13534be97553189a9571ac258ecd2284d24e13e33ed4d2585a2`  
		Last Modified: Mon, 12 Jan 2026 22:26:54 GMT  
		Size: 2.6 MB (2649781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b78878c7014fe78e046fecbdf9c8636ee691a7a769dcade1667a0271322c9b0`  
		Last Modified: Mon, 12 Jan 2026 22:26:55 GMT  
		Size: 16.9 KB (16855 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4167df948ec90f5b1d03f945524ea66706693cf00f34aae30737004931dca60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257958215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60585ec4bba971efe1c0608c1efa6812468809ead10ce360e7f66c9ef6b2616c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 12 Jan 2026 20:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:09:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 12 Jan 2026 20:09:30 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:09:30 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:09:30 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:09:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:09:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cae906e12c91e97dee95b0c8d8b07000fe75181d03a02d2cd0b6126f98cab9`  
		Last Modified: Mon, 12 Jan 2026 20:10:06 GMT  
		Size: 3.9 MB (3851941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51004084767c64bd98e0899a671e18728dafa4df98973970e261982ae4c79b6a`  
		Last Modified: Mon, 12 Jan 2026 20:10:17 GMT  
		Size: 226.0 MB (226004064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0094eac3b5dcf5800c4159034f6102441620a85922290e86c3212ad984f0a44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7338bc9c391864f28f8c706f609d97d213a54fa53e4816bdf8e00f4779215375`

```dockerfile
```

-	Layers:
	-	`sha256:185d2d6e7f8337a77803be1701b8cb65bd80379b64ebbe2830c61f62bde2c396`  
		Last Modified: Mon, 12 Jan 2026 22:26:59 GMT  
		Size: 2.6 MB (2649415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bb2a932db0f8c6b34332dbb5bb27f7286400d5665049e91047fc6b13b6a5df`  
		Last Modified: Mon, 12 Jan 2026 22:27:00 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
