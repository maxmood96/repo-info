## `openjdk:22-ea-34-slim`

```console
$ docker pull openjdk@sha256:6f9b31f40cfb2447ddc1f161a2157f441d0ac91bfd94ce31679aeba1d9f33975
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-ea-34-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:1a5b73df4f135acd8f4ae94870cd8faab750210b4f603f0ce6073996c2a9724a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235910073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451baa7446e6993530d655767c4257e3ecb3e2afe7accce5080620163b62d6f4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 02 Feb 2024 19:48:11 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='170b7192de3e30c796b95d765b12ca457d3f4b05e97bee0bf81709c8b43cd992'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='63460b6a2c4d547d7a8cf4cf86d67a46f5e6a96a62843a787a2aabdbed4df119'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74904b79e503ff6a271cc99326c8d85a81a95e828370ceb3e29839114a34602`  
		Last Modified: Fri, 02 Feb 2024 22:53:34 GMT  
		Size: 3.8 MB (3821597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb48597476cd83603e370cb04fd4ea06aab3bfba8c792623747a02a3fd4c3f6`  
		Last Modified: Fri, 02 Feb 2024 22:53:37 GMT  
		Size: 202.9 MB (202938011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-34-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:61d08af846b93a8387a060d79ea2e54e6c9d38a92c88bffa32cd0c94c6a67288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea62c07341d3cff003ce8d146e53ad3d632b150f752446cbac2dd844563c8ecc`

```dockerfile
```

-	Layers:
	-	`sha256:90fd3d59ab7123b3b2c58f3fb2beca820171428fb0d44a406f44be3bea1d1e60`  
		Last Modified: Fri, 02 Feb 2024 22:53:34 GMT  
		Size: 2.0 MB (2037194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ec0fe16eb66e72143d006ddc5406abe9dc1d7d96a0d584a833c271be7ba6ac`  
		Last Modified: Fri, 02 Feb 2024 22:53:34 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json
