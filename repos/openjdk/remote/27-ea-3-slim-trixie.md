## `openjdk:27-ea-3-slim-trixie`

```console
$ docker pull openjdk@sha256:73d106fe272b475699d596996f1a478e32bc57c6e2f87f00ea25a401c03c3abb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-3-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:92a15fc76533cefaa5f04ffcdf4f3590a32ddfed68d93997bfe6bd048fb97a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260248011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8092dba0bbac5af6d22c72854102a4a5048122037333b5e2bceb425a8d1a7f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 05:19:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:20:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 24 Dec 2025 05:20:25 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:20:25 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:20:25 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:20:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:20:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33059d660e6591aff1f40b2e54ea1455db58a02650a7aa50ada110337cea4c71`  
		Last Modified: Wed, 24 Dec 2025 05:20:09 GMT  
		Size: 2.4 MB (2371061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddb2f1eb8cda0cc9566bb1cf920ae46b9710f1b6be211252699d1e51d7771eb`  
		Last Modified: Wed, 24 Dec 2025 05:22:54 GMT  
		Size: 228.1 MB (228100454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d53d7b93fc879e34103fb0f46dcdb3488d3663eec796458e1bcf12db7bd2b529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92299f8b804dedba3f86b43f533d911211d10ad813fd04b1d266dfa2379bef8a`

```dockerfile
```

-	Layers:
	-	`sha256:7be97cfa7af6eb97cd18cf778dec2a70e510de838a0c8bd745f794cc1b44de8d`  
		Last Modified: Wed, 24 Dec 2025 07:26:47 GMT  
		Size: 2.3 MB (2278777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4149f117ac0de4822406e9ff87396dc41ffd7dd17ed94b9d634de37df13f8c7`  
		Last Modified: Wed, 24 Dec 2025 07:26:47 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-3-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:43c80e9307a516a622066f141a80b68cd1413de6ee5901724c25ad545dbb20ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258473359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8caa320e5047a572a6f139e4fa73f82877f4e5b2f0294f17dc140efc0e6d19b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 05:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:21:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 24 Dec 2025 05:21:43 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:21:43 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:21:43 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:21:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:21:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dae3763c6cfc0a70599264173d388caee7f2d71d451171865652c3d3c2b13a`  
		Last Modified: Wed, 24 Dec 2025 05:22:12 GMT  
		Size: 2.3 MB (2314073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef4631890a2d33a9e24d25a169b74565c0eb6b6f8c917a899e5818fcc6a20d4`  
		Last Modified: Wed, 24 Dec 2025 05:22:17 GMT  
		Size: 226.0 MB (226020658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:71d067a57eca5a4ecc6aeb19542c92c6d94b4905ddd614f759600fb18fa881d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d303418690e17579f203507674efe408b1de0a2ce9b2eb83b7f1c9cb5118d62`

```dockerfile
```

-	Layers:
	-	`sha256:89e2e657e140b668ea1b1f06851978c436b8e7d05fc1c599fd4c2fd67c5809c5`  
		Last Modified: Wed, 24 Dec 2025 07:26:51 GMT  
		Size: 2.3 MB (2278463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9a3e0c0b405f63bb1ba44315a3a96e0d3bd5a5486bbad312ba45aada3706af`  
		Last Modified: Wed, 24 Dec 2025 07:26:52 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
