## `openjdk:27-ea-24-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:1fc40eab8174b8d1d613dc0dc9b6b0c1ef9fdf9a7ee2f45ff9603c0e77fae8dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-24-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5c1fc1d8021d6bff05c11367f4be5e4fbcde8edbb09253a6de1cf93425510c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259311424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745f836dcc1b9f3396528720b64a312fb02c695f930fb22976f326f74c19c56c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 07:12:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:12:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 02 Jun 2026 07:12:38 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:12:38 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:12:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:12:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb554138a9c587a26573d1289b6099b4759851a782ec8ea9ecd546559e04f2c6`  
		Last Modified: Tue, 02 Jun 2026 07:12:59 GMT  
		Size: 4.0 MB (4032657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1345e0211d74720fcb5914fd6c35cfb1b33a3bf99c1b26e8a7e5df2a798c560b`  
		Last Modified: Tue, 02 Jun 2026 07:13:05 GMT  
		Size: 227.0 MB (227045224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ab7e3567e688d6251b62d6e3a97ab2d87f46bc6e9cfbeebc8b3f77a0d0c75d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea9c4abc2f2e58718dc0bf4f016469ae6a6604a04ff284426b84844ccb54ba2`

```dockerfile
```

-	Layers:
	-	`sha256:355b1e9c8adafb17fab9aed9472798e917c7c595289b638ddb5129af870d660d`  
		Last Modified: Tue, 02 Jun 2026 07:12:59 GMT  
		Size: 2.6 MB (2647272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e61597391adb40b0fc420af84f9a6273e96d8037d7fbfb322de08cb9a11ea1d`  
		Last Modified: Tue, 02 Jun 2026 07:12:59 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-24-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6674911f19f1fa3bdda3b06e1c012968bddcde76924cc2a432c9c0e0e8a110c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (257030218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc0a403c40f01f3559fb7da92321e9e7d52231788bfb38d2ea86a5a9af176a3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 07:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:12:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 02 Jun 2026 07:12:19 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:12:19 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:12:19 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:12:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:12:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192faea0e376750e42dddbfd3a93cac43e15a1f03755f125954bb7f984149278`  
		Last Modified: Tue, 02 Jun 2026 07:12:40 GMT  
		Size: 3.9 MB (3852975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e18d91e9a14ab11360b9b38a05fc977f70254439c5cd0d67ece106a03e1afe8`  
		Last Modified: Tue, 02 Jun 2026 07:12:45 GMT  
		Size: 225.1 MB (225062200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:78c117bf005d6fe2aa68282e129fbe1e1ce8654cb949ae4b47e0de259505a3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a8d2c9ad627bcbf327cab03881adae6d6bc6ab7dbc4570b991595c97c68e28`

```dockerfile
```

-	Layers:
	-	`sha256:b56e76ea0b280bbf32800dd153d28af68eacdebb233410377e57d09de0019914`  
		Last Modified: Tue, 02 Jun 2026 07:12:40 GMT  
		Size: 2.6 MB (2646906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cb4b4645f06717658a0fa8d72daa8ec71fbb584cd6ed8e26049e91a10e5bd4`  
		Last Modified: Tue, 02 Jun 2026 07:12:40 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
