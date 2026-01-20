## `openjdk:27-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:4df75d4326584d03212133d648b9d36ca37eb934893e62d9f7112e38b73dc98e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:c3c5fe3e3997a1186f24de2d4c73bdb05ce763891598d20b92e582611e0b5183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260227301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0b49a9b9d09ea1b8e36063669ac284cd313b347435f7f846d9991b9d89c948`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:44:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 13 Jan 2026 02:44:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:44:41 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:44:41 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 02:44:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 02:44:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb58c168ac4d84ff3d1431dfec13fb3886cb8244a652d452ba18f417ff044e32`  
		Last Modified: Tue, 13 Jan 2026 02:45:01 GMT  
		Size: 2.4 MB (2371012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a769d0f4615c1c05cb31c3698effcfe961ef19cdc45ec6b184f471db5b41a0d4`  
		Last Modified: Tue, 13 Jan 2026 02:45:36 GMT  
		Size: 228.1 MB (228082604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:47b5ee4cd95ce1ea6e5a37e47dce26055c5cd59e4375d40e4682d9064151c06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b86a404e373d510496e73d7de21fe1f01ff43c32f3894296dcd7b00449b24f`

```dockerfile
```

-	Layers:
	-	`sha256:6d509c8265dba3122525b1947f4f2c62d07d54058d9febcca62aea218a813551`  
		Last Modified: Tue, 13 Jan 2026 04:25:09 GMT  
		Size: 2.3 MB (2278839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e497f84e036bccfb4c51c7f2cac18b9f58a5c7457be40ad2642e24f1d31e767`  
		Last Modified: Tue, 13 Jan 2026 04:25:09 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c9bd8f190979be2a54511780ed2dbf6872d28f2fad4e1e6223013f10016b5b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258454118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e7dd127a9a2bedfa128ff1e4fed74a5038cbb8bdcfc93271065e58ca48f572`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:46:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:48:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 13 Jan 2026 02:48:59 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:48:59 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:48:59 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 02:48:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 02:48:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7aa79147dad9de2119b1d63806a41e74d82c519bc5d0e22b52d3ae092846f`  
		Last Modified: Tue, 13 Jan 2026 02:47:34 GMT  
		Size: 2.3 MB (2314124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828a39f22e5c8b43e17cc0449e457836d38558fcbc6ae5434e84a2a1296f037b`  
		Last Modified: Tue, 13 Jan 2026 02:49:50 GMT  
		Size: 226.0 MB (226005952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:7523b6f4f95287daea3473a17bd272bfe380cfcf44134f6f1eb6374013d6bafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e8d7fd6fe62aa7f69c0f4d4d5e0d96c0d5c49735193057edf6837381deb335`

```dockerfile
```

-	Layers:
	-	`sha256:93fd3ebe084e1bd5431ddcf375247bb0fd9b8e6bb947c6a429c806b436d30a01`  
		Last Modified: Tue, 13 Jan 2026 02:49:21 GMT  
		Size: 2.3 MB (2278525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09908f5f61246885d60483c5338bf87dfec8bff755f27ef7b738a2bcf5966f49`  
		Last Modified: Tue, 13 Jan 2026 04:25:14 GMT  
		Size: 18.3 KB (18254 bytes)  
		MIME: application/vnd.in-toto+json
