## `openjdk:26-ea-29-slim-trixie`

```console
$ docker pull openjdk@sha256:d014f1a27a104ddbe654e62e77213252bee02351048af1a2d06cd0e58e5774cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-29-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:90eba6245fa1202c8ffd417a674e4593c0d4f219ef0e0b4e88d964201746938f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260155188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3d4e4a684d4a0edf9fc295f4c3b58be6b74ebf29baedf2b5bdfda5662ca5bb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:11:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:11:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 30 Dec 2025 00:11:39 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:11:39 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:11:39 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 30 Dec 2025 00:11:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 00:11:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be35d9fd94d0e7aef88d5a2f7be951433de9300324957479dbf67784181f552`  
		Last Modified: Tue, 30 Dec 2025 00:12:11 GMT  
		Size: 2.4 MB (2370972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05bc995997a92d0f29ab87820d69d8b53123b88ec40fbafd6a881e625f1799`  
		Last Modified: Tue, 30 Dec 2025 00:12:28 GMT  
		Size: 228.0 MB (228007683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:f17bd9857688e6c7444745332c462de6d53fc960f179fae994858be69d04e87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8377ecf71d156a5186744a76b4caf11a85a39bbca8536ecee8b5f26cc15981`

```dockerfile
```

-	Layers:
	-	`sha256:0f63e7d885b5d8ecfa2b7a210beb39a9c1ebb66e43f5079fd45a32d856efc9a1`  
		Last Modified: Tue, 30 Dec 2025 04:24:09 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc4111b4f11257ecfb84553508f3ef9a4e305d1f4a484c4ffccffbe21070b06`  
		Last Modified: Tue, 30 Dec 2025 04:24:09 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-29-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:399b8d3026b9f66b31a76781128c7289ae894112e204be8b1910cec26999f16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258369126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8380fd7fc59240d35d9a57e88bf0927e87f908377cd3b6dff29b46a04a15a355`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:12:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:12:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 30 Dec 2025 00:12:31 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:12:31 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:12:31 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 30 Dec 2025 00:12:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 00:12:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aabdee59c6729da2d6bd2e193e295267ed4c51c853e096082c7b274b404b2d0`  
		Last Modified: Tue, 30 Dec 2025 00:13:02 GMT  
		Size: 2.3 MB (2314071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbf8a36c7a56741516f3a492a41ade1fcbc78e313c30901731933badc105022`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 225.9 MB (225916419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:60ffe5b91b5ac4253e5a78d3e34af51954bb5fb97e4665dcc0f5e778c2fa30a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38286db264e724b191a44e80a3aa7b456c0454022a25d08fdfae8803148938a`

```dockerfile
```

-	Layers:
	-	`sha256:a23c8afc1fe46006f4b67ee8b790c738f44bb96ddc93da94b5bf16bcb5cc02c6`  
		Last Modified: Tue, 30 Dec 2025 04:24:13 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262dc50b3cf677ad610590f4e3fd857b15a7dd5d0d89b6dbea8132f58140667f`  
		Last Modified: Tue, 30 Dec 2025 04:24:13 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
