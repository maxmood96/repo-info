## `openjdk:26-ea-30-slim-bookworm`

```console
$ docker pull openjdk@sha256:f5c92986a0e711e2b7490a0cb4ca5187e7084d221c9aafbc1db8081c7e190141
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-30-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b677c335ee23fbf1aff3d595413275cabb0c8f60a2202d95f1349c7e77d051e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260270669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b621cefeed286fc4e4b0b4c6cc342fb303712dd3bfc79af94ea3a6052a224481`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 12 Jan 2026 20:07:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:07:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 12 Jan 2026 20:07:45 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:45 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:07:45 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:07:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:07:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41305c18a9fb68146c822ad773b953451510b0fdaa14acd948548efab91a6a5a`  
		Last Modified: Mon, 12 Jan 2026 20:08:24 GMT  
		Size: 4.0 MB (4028226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3442becc04a99bf45fa4ad048589c5ea4043abb73601c0dcdf5b631b4a0a154c`  
		Last Modified: Mon, 12 Jan 2026 20:08:54 GMT  
		Size: 228.0 MB (228014019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a0ee7e37d84bfce1b0f4da36ba054838b68e2dd4438a8d7fe5471455b950044a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5352392ac5058a0dbbe0ad9b7a51c435bd71b0c544b3aaa1a6c6cf03bf017956`

```dockerfile
```

-	Layers:
	-	`sha256:eb1ce4d175c20afdd547009e8d2dbc0bdb61726ca29054c96533ce5835005d98`  
		Last Modified: Mon, 12 Jan 2026 22:24:23 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a168b62391b9105e6569527eaad1beb17f8a391d817ac5a5b2acaced0d7ed5e`  
		Last Modified: Mon, 12 Jan 2026 22:24:24 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-30-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:af56d4274460805fe6fbf6affe82eac00b0762a1a597c1da7003d7107e504aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257888669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5076e4a186a65bb0d55f54d8014626e546e28749f491c859310f6dd96f8a6f7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 12 Jan 2026 20:08:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 12 Jan 2026 20:08:32 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:32 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:32 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:08:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a37c1bc352ab9da4cdbb9bdfe7eb57165e70f0c70b9afcb74bb969d84e90ef`  
		Last Modified: Mon, 12 Jan 2026 20:09:07 GMT  
		Size: 3.9 MB (3851943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05eb9dcbe715054965773f5f7293ef68b2fd2bb79ea334db17c72ab967835ef`  
		Last Modified: Mon, 12 Jan 2026 20:09:14 GMT  
		Size: 225.9 MB (225934516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e2cf9d58e42673833e2930425501bfa32c467ddb90d0f9924266acff4f013547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40253292151d62589cba0c19d0ca32225a99e4e1b9f9de41568e1e3119f3878f`

```dockerfile
```

-	Layers:
	-	`sha256:7f35f951452c2aebc90295cd59a73ff4aa3e637773bea783ccd162e2508a5060`  
		Last Modified: Mon, 12 Jan 2026 22:24:28 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5813b2231059f6d122f86ff39c9e9ff4bfe10d36af6a5ad216232ea6d04cbb3c`  
		Last Modified: Mon, 12 Jan 2026 22:24:29 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
