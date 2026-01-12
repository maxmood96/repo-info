## `openjdk:26-ea-30-bookworm`

```console
$ docker pull openjdk@sha256:198d25dde1a3367e8e9f2b95db7d44a8a1e89d164f2ef283933dd5717e301e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-30-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:7771b52c7e3fa146b75d6a36da637a2feb65d201198f54a84f57f7635f7db063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.8 MB (381814854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34255ca1fcf004cf1d984cf71164c294404dc8b1a7c365b51d20357d93c86506`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:07:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:07:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 12 Jan 2026 20:07:44 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:44 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:07:44 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:07:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:07:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693876f29a36e2c153d15ae43ed5d95f7cded2b8cbe9f4f082dc06590a8cf0f`  
		Last Modified: Mon, 12 Jan 2026 20:08:22 GMT  
		Size: 16.9 MB (16944771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fab1d126efc9402ab80e8df1e8f451a92fdfb3331a49a675b8672de8c2cc992`  
		Last Modified: Mon, 12 Jan 2026 20:08:50 GMT  
		Size: 228.0 MB (227963853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:65b4bea73530a83a3cf4fbca5a6174438743b8104e09c92d24973366d2af8a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ef66e8a0aba73d4d68b9eed21ec69ffd391d6c78367981ce3dffa40b30c513`

```dockerfile
```

-	Layers:
	-	`sha256:f5028122bed4a8672c73a68fdad7e74d0f5d294b9fe1a0d8cc276879ecdbd700`  
		Last Modified: Mon, 12 Jan 2026 22:23:39 GMT  
		Size: 8.7 MB (8668236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80236c5b5b0150f066b787c342d0c644cfee0213fae44d39f4fa5ca8b6505229`  
		Last Modified: Mon, 12 Jan 2026 22:23:40 GMT  
		Size: 17.9 KB (17938 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-30-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:218e0350980bdeae01aac5df0ab21888fdc0af5779b62883f423f6a022c7303c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.9 MB (379942450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30769cc16a706fd61bdf013b4e1bddd6f18a5209fa09cd54e9b3809408cefa7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 12 Jan 2026 20:08:32 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:32 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:32 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:08:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d741a504486261440e58f0e65094a42fbe2979ba7ca6a3ea8230f0c4e85e51b0`  
		Last Modified: Mon, 12 Jan 2026 20:09:12 GMT  
		Size: 17.7 MB (17728520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea63a28d6c28b0f7146a7f7911daffad4eb071e5974b0db0f7670f4b225d198`  
		Last Modified: Mon, 12 Jan 2026 20:09:16 GMT  
		Size: 225.9 MB (225885235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:886fcc8ef98fd328c7c86130ffb200c6d241b0b3947905f0736ea65fb0d828b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3938244d9901687860cb957ddf0c574dbe04c7f5aaa97221d9b28bbba47327fc`

```dockerfile
```

-	Layers:
	-	`sha256:4bc7a48817f329dd63710368732d2ce201a0dcb9e623bc88d2b9efafd40fea38`  
		Last Modified: Mon, 12 Jan 2026 22:23:50 GMT  
		Size: 8.8 MB (8805081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827a47b06d464920696292bfb416ea62c9bef431e99fa779014b75a51fb97301`  
		Last Modified: Mon, 12 Jan 2026 22:23:51 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
