## `openjdk:26-ea-29-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:746e34d7eaa69d71ffb0bd97dc3d806c959b098a40b23d5398414a2c04e2274d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-29-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8cd46070fcbb6508a51a0bae492f891ee3f776c023dfe7b60b771ee50967f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260259862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bc0bf8a568eb1ae6a9ffa57eb5e0b2818c214a8dda1f809f10cd87fa9bb022`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Wed, 24 Dec 2025 05:20:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:20:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Wed, 24 Dec 2025 05:20:18 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:20:18 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:20:18 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 05:20:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:20:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f004fe71f1031e0adb68819e4effac6b8eb2ea2720512304328939e32f605eb8`  
		Last Modified: Wed, 24 Dec 2025 05:20:49 GMT  
		Size: 4.0 MB (4027340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ae8d94f5a02a383f6cbe2c4c44e8bc8e9e7f80c7265591c6b62bba9ea7b076`  
		Last Modified: Wed, 24 Dec 2025 05:22:26 GMT  
		Size: 228.0 MB (228004104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4c7219809ccf994f56854caee8935af96fdca101a937aadc4e258ff2678c713b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8486124ec6f7ef028c0c2a9a1c45f1c4364aecf825e27503b2d37e28e508f7`

```dockerfile
```

-	Layers:
	-	`sha256:888ea2c180a92b506a5b3c718f72f53cdcaf74685f8374289f181742854fd887`  
		Last Modified: Wed, 24 Dec 2025 07:24:16 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436e1a823694438ff0d7d9d2c57b20f0b9ce4907762d37b642ac2247d0be357d`  
		Last Modified: Wed, 24 Dec 2025 07:24:17 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-29-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f17d00ffb4d7e4865b1886ae8199e5be7ec45a19bd8ba4c9daec59b9e750369e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257865869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630b865b522e2745a61896f22555879303720b16f557c74349a8d82e56bb91a2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Wed, 24 Dec 2025 05:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:21:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Wed, 24 Dec 2025 05:21:31 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:21:31 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:21:31 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 05:21:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:21:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5849b43d5c897c8d3702110a9872463614c5c2d926ca065b8c1cb0ae25b1760a`  
		Last Modified: Wed, 24 Dec 2025 05:22:03 GMT  
		Size: 3.9 MB (3851384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617932b18cd07f3f9790ccad4a739fd4ecc94f46261c37712607ac1df5445ccb`  
		Last Modified: Wed, 24 Dec 2025 05:24:08 GMT  
		Size: 225.9 MB (225912256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:469b8f5f6115488be9d755cfff010184736fa5f43a18a4e7b896deba8237ddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783a62350c9c06c1f2f50991550651b2bd2d624a1341ce238a5566b04a12cd0e`

```dockerfile
```

-	Layers:
	-	`sha256:6ef3ac18d03909e957b7ab6fab61e92ccee13b6109f0839c430e736e006f87e8`  
		Last Modified: Wed, 24 Dec 2025 07:24:22 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7922f408dec3f6a75bff57cb7682eaf8badae99c0111d25f9dc8772654d57135`  
		Last Modified: Wed, 24 Dec 2025 07:24:23 GMT  
		Size: 17.0 KB (16989 bytes)  
		MIME: application/vnd.in-toto+json
