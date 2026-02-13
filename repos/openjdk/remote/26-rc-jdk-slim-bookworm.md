## `openjdk:26-rc-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:67aa1d07024d4d1cd2a6e86d0ce76f0552759105d19d67f7d583f3c6d75f5dee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8e1208449a70f98f93d941d25e98d7c7e2f090493b810657fec0094385a23bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260293102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b9e4ea8452670b5059b7de98d27ce4da7e05ea0cbbd628b6b67fea6f35369d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Fri, 13 Feb 2026 00:01:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:01:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 13 Feb 2026 00:01:25 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:01:25 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:01:25 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:01:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:01:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc02d0117eafcd01a3a9e4a01e78b3efa96ac4f02ca98ee0846fc345cc5078c4`  
		Last Modified: Fri, 13 Feb 2026 00:01:45 GMT  
		Size: 4.0 MB (4029195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45915bb3f007b9126ecb5c745ba7042d9cd68721559aa71e340d62d1d92b607c`  
		Last Modified: Fri, 13 Feb 2026 00:01:51 GMT  
		Size: 228.0 MB (228035420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4abafa33e5a8d9ef2f907fd7b4afd2caaea1bd3edff982c68a48d25a4823500a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9498ba962fb89b0a0ca6ec0f8239a5c8822b68f243cbba184603bc20856444b`

```dockerfile
```

-	Layers:
	-	`sha256:fa54f4f893bcb8ef21f304ba5e5ac4faec9cadea72406c0ba93c3ee1f6f65a9f`  
		Last Modified: Fri, 13 Feb 2026 00:01:45 GMT  
		Size: 2.6 MB (2649115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbc33b1bbadbeb23aeaf9ec2f72114fdb6fd6c4b3d859aca8dc309b4f3bff52`  
		Last Modified: Fri, 13 Feb 2026 00:01:45 GMT  
		Size: 16.3 KB (16267 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7cec4114ec7973295bd062a2466be43e0f67eb91527475c80caba721e79ac2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257912253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec6b1903ff654476d09a31b157c7e03e3242f9c0b5f2774ecf08fcc6b5f568d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Fri, 13 Feb 2026 00:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 13 Feb 2026 00:02:45 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:02:45 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:02:45 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:02:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f407202ab4af01f02e82832f35bd0d33ecebd6a98d7edd913210a568c88bf9b`  
		Last Modified: Fri, 13 Feb 2026 00:03:06 GMT  
		Size: 3.9 MB (3851968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae72f9975d5fe249e1a46d5ecc8f01a57e4a47cace5c4a56e51f86031a8d5600`  
		Last Modified: Fri, 13 Feb 2026 00:03:09 GMT  
		Size: 226.0 MB (225952462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:24c5fb48f310158b4b3605b50ee7aff6c6870e80622cd734f6fb6d646a7ff950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a0de089f217db9170f08b830bf47a960ccc5d7eaddfb73ef9340ff158347a7`

```dockerfile
```

-	Layers:
	-	`sha256:30d40e005d75aab472008cc2f506e9d19dccf1abc696be34bd62ccbe475510dc`  
		Last Modified: Fri, 13 Feb 2026 00:03:05 GMT  
		Size: 2.6 MB (2648725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7224cb8bd4c473ab17d595d521606640ef720738bac8192c8f608aa9119e61`  
		Last Modified: Fri, 13 Feb 2026 00:03:05 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json
