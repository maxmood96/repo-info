## `openjdk:24-ea-4-slim-bullseye`

```console
$ docker pull openjdk@sha256:5a98cdde92578dfdcc30b84f8ba3cbdc38467fc6051f37fc5e52bb10cbec3b14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-4-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:137d4de732179565436286a3db611c2d3a1e0246176be25daaef5f0cbb0e870d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244480713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f95324a6ca0cd9b91e195578b5257c98fa58bc754e831cc9ac0ba977e10efb9`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:52:17 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f7d5e62f73829e2b3ce5f829ea579dc6a0a7dc2c0042e60725de08777741a`  
		Last Modified: Tue, 02 Jul 2024 03:21:10 GMT  
		Size: 1.6 MB (1581765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43640ececcb4455de5752a88a1d13f75ef4fcf8a851352570a77ef8dfc5e1f15`  
		Last Modified: Tue, 02 Jul 2024 03:21:14 GMT  
		Size: 211.5 MB (211476664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-4-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:17a006cf9594befacd7dea0bef9b4d6548275be6f587e0ee9cec1de60b386466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffd25805e14653b2e20338aaa8b18fc1122a4035b1b1621a95cac5ad9d46061`

```dockerfile
```

-	Layers:
	-	`sha256:04b6464395b3113c5b1ab2f8d032acaabfebee45e76686eab62832621a304dbb`  
		Last Modified: Tue, 02 Jul 2024 03:21:10 GMT  
		Size: 2.6 MB (2638489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f8418f1c069f00af6abdf32ca130461d23c65bb02866a64feec525ff5977c8`  
		Last Modified: Tue, 02 Jul 2024 03:21:10 GMT  
		Size: 17.3 KB (17345 bytes)  
		MIME: application/vnd.in-toto+json
