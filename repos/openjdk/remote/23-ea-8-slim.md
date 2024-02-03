## `openjdk:23-ea-8-slim`

```console
$ docker pull openjdk@sha256:262b8afb5d30e04fa86296b49419da06e40206e0f097590639dfd69387cbcd88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-8-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:5d3f99602be25011d8d44b86679a302eb1b9d7d4e97dd7d28de4245c0828b302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236281058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901e5b31da455be51055b534b266c15298f9c46ae1ca011a2e3de7b45b849493`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9d9b96adf8201958d2131d28dde1f97ea4d43c9255d51e0a49e94b1f15d32c`  
		Last Modified: Fri, 02 Feb 2024 22:53:27 GMT  
		Size: 3.8 MB (3821598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b829526b78dcbb5070dd65e7ceb734428149d8ad3c274e475aa108b270995c4`  
		Last Modified: Fri, 02 Feb 2024 22:53:30 GMT  
		Size: 203.3 MB (203308995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-8-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:c99982f65e3e0839f8d869b41b5b375ee5f0780a80ab36f227c0218275c8ef09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d70e340cb193e85554365e78e650998393e8e8f756340f98dd1503a930b48f`

```dockerfile
```

-	Layers:
	-	`sha256:46de691b93b5d015b5beddf3e1f2d55ed2a7b3cc43146b0db192720bdddc1ee6`  
		Last Modified: Fri, 02 Feb 2024 22:53:27 GMT  
		Size: 2.0 MB (2037182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb8412daa9f47d477dc017b23eda5163b6274fdd3551702802be30d04bae619`  
		Last Modified: Fri, 02 Feb 2024 22:53:27 GMT  
		Size: 19.3 KB (19325 bytes)  
		MIME: application/vnd.in-toto+json
