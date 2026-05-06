## `openjdk:27-ea-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:ff69d908d01e2c162db7fda3d59f37f85e59240684b094deff77795c00e796d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:2278fdcf762c1942db5002774d022b1ada8ab11476e6764c6977762f7f411394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260794104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12a6ac7662b3fceaa836cb7ec2c24a3a2ab2fa13558f3b309c9ad77cb317971`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Tue, 05 May 2026 23:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 05 May 2026 23:04:14 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:14 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:04:14 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:04:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:04:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbe942486324591bc3f52a508dca557ff255db8c113223e9887bb7275a90048`  
		Last Modified: Tue, 05 May 2026 23:04:33 GMT  
		Size: 2.4 MB (2371175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9974b10904011a3e8336d9bd9321980b78b796803fcda8f2648b662f243f93`  
		Last Modified: Tue, 05 May 2026 23:04:38 GMT  
		Size: 228.6 MB (228642755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:5a85c811925d5ac982848cc03785d870caa3ed1cf26a4a0aa3b3f30cbdd0c058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796e9d9589ead7786b7fe17ecaf7b0b044f2d58c6cd25e6362e397d3927108fb`

```dockerfile
```

-	Layers:
	-	`sha256:a932dce891909f20f95d4b4b03658229011bb31be887208f2b21061ad69a4d31`  
		Last Modified: Tue, 05 May 2026 23:04:33 GMT  
		Size: 2.3 MB (2277625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5a3ff13a9f991d47cf1c714c7fc6e6b4c38c982e1b3ce4701716fa8766c5f1a`  
		Last Modified: Tue, 05 May 2026 23:04:33 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:997453e9d485508c03598cf5578b3ce3b07f432a103a2d9f246dc2889db345ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259061093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ed501c03af1f4beea2a24ff22717a1cd2535d275036e7ee3593167c81bed7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Tue, 05 May 2026 23:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 05 May 2026 23:04:00 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:00 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:04:00 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:04:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:04:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f49adad38b9aa12059c54873fc37fd827d99ed3dd52dc4610c164ab1980695`  
		Last Modified: Tue, 05 May 2026 23:04:24 GMT  
		Size: 2.3 MB (2314395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ccc4a7cd2e1bc6b4971bd326ddb52d3334d5a42c3dbfda1f5fa8cdb787fd0b`  
		Last Modified: Tue, 05 May 2026 23:04:48 GMT  
		Size: 226.6 MB (226603092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d5fc8adf629baa9ddfa4b1a997c61513e3067327f65d7c4cd7874abe9e886fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2960ecb26e6f7446dfefd5307398b114b0ccf4ab6e3dc442aec48bf87268c116`

```dockerfile
```

-	Layers:
	-	`sha256:66de370fae32ae6991ac8739327b6b9b09951f21f7153eb13ed648c597fd97cd`  
		Last Modified: Tue, 05 May 2026 23:04:24 GMT  
		Size: 2.3 MB (2277311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66200f5a721232ec8931b5b46da7ae52677da44f5736d84c694f7d00b57adcfd`  
		Last Modified: Tue, 05 May 2026 23:04:23 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
