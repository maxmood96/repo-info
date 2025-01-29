## `openjdk:24-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:6af3c3f721ee1fd2fb637288884a507e2b91d097422cfaa1b6bfa393cc95ee77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5973bb30eda8f8373e278da4a729ed1af0cbe35449c398aa383e2e9e8fbe92b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366775082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd74efa291c98fb450bdef416f0f00d1b36b322b31b59f4a6c78307d92b230f9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e816e9be3272263f3efab343ca692a3b4ccb3a71496f93649873219c5e12fc89`  
		Last Modified: Tue, 28 Jan 2025 23:28:23 GMT  
		Size: 16.9 MB (16943050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba27295ec43c5a7a8e3a2e7fdebbddb63587bd29e03429070454683a6101aec`  
		Last Modified: Tue, 28 Jan 2025 23:28:26 GMT  
		Size: 212.9 MB (212894747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:be261b095a077b00566197974b96faf2adb9a3901441fc6bd2e0c433f87a03da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8454870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25406e8acd57ccee190b35f3d544b3bfab77c8df3c2c44f4524bce63eae058ef`

```dockerfile
```

-	Layers:
	-	`sha256:0d36d984e3f69a19671b2f6398c35a6c5b7c14685f402fda3f71012558eab224`  
		Last Modified: Tue, 28 Jan 2025 23:28:23 GMT  
		Size: 8.4 MB (8436252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d727af2b3ee30950f39a3f0c7f48ae4bbbd5873c8f6788408e1edd072a3aa4b`  
		Last Modified: Tue, 28 Jan 2025 23:28:23 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:95a59318480fe00e7fbec8b59c0006ba1fec4fa8ebe55149406d32aea4136c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.8 MB (364841405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b510ba9f4e31f62da3d3f6cc9cd2e60f58b8b32a7c8818ce65ac2a2052f9e432`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6a2555d05d59a1b517aac5c56ae999793d8ea02a417f7a16f4c8c2080cafbe`  
		Last Modified: Wed, 22 Jan 2025 02:32:06 GMT  
		Size: 17.7 MB (17726678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f950deb0010b9b7aeb7e5cad99b5bbcc9ec71a4d54b09dbed79f0dfa862a3c8`  
		Last Modified: Tue, 28 Jan 2025 23:39:45 GMT  
		Size: 210.9 MB (210853173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8507d91ce0e0bc372f2373ecdaba151140ce368ea04a2f122726f43b00975053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8591881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ce9a50a4929ee3f916e419bf64efd5deab57dbd33926801738651b39502bb1`

```dockerfile
```

-	Layers:
	-	`sha256:8056a04b77053c369897cf7a7b2c72679c25869c4aed2a8823576f31581b2049`  
		Last Modified: Tue, 28 Jan 2025 23:39:41 GMT  
		Size: 8.6 MB (8573120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594756bb5e5014c29788d22f9205fc82e3e5f73b2a4fcc291fb47f1f2092cc52`  
		Last Modified: Tue, 28 Jan 2025 23:39:40 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
