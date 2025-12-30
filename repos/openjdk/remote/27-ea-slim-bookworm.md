## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:129ee2df42fcb43ecd2050c5ae977df6fafa4742a9b842bdd931b6c4833eee14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:9b21380b56bb1aa5397f2f5916cf0fee549630c2213abca85bd4f36a373440d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260359379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f338d39d7dbc1ff0240e81fa084b20164f0b4dc404d8bbb26a616ab6603aaeb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:11:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:13:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 30 Dec 2025 00:13:49 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:13:49 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:13:49 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 30 Dec 2025 00:13:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 00:13:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998fd0232716ed617e4a51b1d2fda0f16db505c6c59da1e1d980d576dfadcfc5`  
		Last Modified: Tue, 30 Dec 2025 00:12:36 GMT  
		Size: 4.0 MB (4027374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d833ff69129232b9dbfd4162e937eb3e19fe5d6db90f36f25fc17e2daef691`  
		Last Modified: Tue, 30 Dec 2025 00:14:28 GMT  
		Size: 228.1 MB (228103581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:686eb5fe54ae91a29c17099a64b5a8d81d4c41cce933669242af8e7fdb0b20fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d81c6d72b4fb997167d83f0a7de67b77b93eedaf60c7e03914312ceb02d145`

```dockerfile
```

-	Layers:
	-	`sha256:d98022eef347ba2bcea4d94e11fd83523aaa35c902ae508133e9bb362d8cf39d`  
		Last Modified: Tue, 30 Dec 2025 04:25:32 GMT  
		Size: 2.6 MB (2649781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb7b5752cc1d7dfde7c80a867ff8f9a4e085a94745f1b8f7cf5c7fd0c0b65e3e`  
		Last Modified: Tue, 30 Dec 2025 04:25:33 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:96d7cb7de8c18bd2ea6df1dd5c501620c38261d9750c65649c4c1a5ad5432cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257971467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37559abbb10b421b13a90f75eef0571d1ee01ee977a7bb6d9e2630d7388fca93`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:14:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:14:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 30 Dec 2025 00:14:47 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:14:47 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:14:47 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 30 Dec 2025 00:14:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 00:14:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8733f32be7a3e46544fc2f2fa6c02da650513b3284d8cc53d6b62147e56079fd`  
		Last Modified: Tue, 30 Dec 2025 00:15:20 GMT  
		Size: 3.9 MB (3851401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183264c38ae927aa4d2e2a4768f36212efb6c3a503a785cf2c747b20457da489`  
		Last Modified: Tue, 30 Dec 2025 00:15:52 GMT  
		Size: 226.0 MB (226017856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1cfda07634ca6d66e651a747c9a6e15e6cfc2c336384ec63b1fb4b9b7e461681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7990cef798968a83ee3642cb59a6d80088bbf1b079b6f427f696e434503fa4`

```dockerfile
```

-	Layers:
	-	`sha256:a444cf6c87ef127e16e5a62ba54e781ffb7fe332249906cd8e74336754bdc631`  
		Last Modified: Tue, 30 Dec 2025 04:25:37 GMT  
		Size: 2.6 MB (2649415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571a0c580c9a41ba8446130e9b6410cc9a41e5293abb65a85ea96511527a4360`  
		Last Modified: Tue, 30 Dec 2025 04:25:41 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
