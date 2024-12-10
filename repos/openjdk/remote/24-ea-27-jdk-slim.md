## `openjdk:24-ea-27-jdk-slim`

```console
$ docker pull openjdk@sha256:2c7e9fb367b7797cfc60565b5a021d21a9bce7c78a8e762e27a2d401208b5798
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-27-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:e2b4a0558cc7e65b422eb4b896093353c70ef9dbab29ecb42510795025d12834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (244954733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc9c3a42d719a3e09fdb5d83e90823d49e1365539be7b9e1b90fda8c689534a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f9c24b35d1fc2642535eb85c7c41e04bf4c5a322d1e5a5b99c9ee400c4ca49`  
		Last Modified: Mon, 09 Dec 2024 23:30:27 GMT  
		Size: 3.8 MB (3824649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbce5faba0cada59211832b93f60c29932344951e03669164017d281af739c4`  
		Last Modified: Mon, 09 Dec 2024 23:30:30 GMT  
		Size: 212.9 MB (212898504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-27-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:0e4b67fba13dfff97032d7f02181e9e423ca1dfbc2ed08a758594a5154c52f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421cab31fafd3b0ee6117afbc65fee3c354a8e41b6abd6a2f1847a5f0fc95e29`

```dockerfile
```

-	Layers:
	-	`sha256:275d09ef84c9c753af7922abf89201ce3cd12797e8053b4c7f8fe77d3e01efc2`  
		Last Modified: Mon, 09 Dec 2024 23:30:27 GMT  
		Size: 2.5 MB (2536770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c1d2301ac47faa9f8de10410484a0da3afeb4d624b793ea50b72a1b01f8f49`  
		Last Modified: Mon, 09 Dec 2024 23:30:27 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json
