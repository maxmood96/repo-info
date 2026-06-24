## `openjdk:28-ea-3-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:2f0e684690b90618c72677b2a76d39e8097fc8ab9021c3249ff18a1f26dc75b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-3-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:4460540f3469330390e9e302e6c91403175c1bf844d85c0f0508faefeb39cdee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259706339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ecf78580587b6c0cd004481ccb3a7294b70dba77bbec5299257b0cbf453327`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:46:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 24 Jun 2026 01:46:51 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:46:51 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:46:51 GMT
ENV JAVA_VERSION=28-ea+3
# Wed, 24 Jun 2026 01:46:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Jun 2026 01:46:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdeba350b5eff3dd3c5c0500e61563608c8d81f360e99e211aaebc9a09856c89`  
		Last Modified: Wed, 24 Jun 2026 01:47:11 GMT  
		Size: 2.4 MB (2371331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2818f57ded9de987e02e9f24c6eafe9d9c5a5dcf229a1a51efb2671efce9f12b`  
		Last Modified: Wed, 24 Jun 2026 01:47:15 GMT  
		Size: 227.5 MB (227549589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d52b1a759d940e4e438f71ba9816b6c859f29262f922079c322cb21da8c52fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75058a74389c165781f27aa229258d74b5a5865f7612dc6b94a274d3e3c79cdc`

```dockerfile
```

-	Layers:
	-	`sha256:4e2564b736cf2b8aaae6c9267dadbaa8662c69a36b5b38d0efc9b19b3ab8cf99`  
		Last Modified: Wed, 24 Jun 2026 01:47:10 GMT  
		Size: 2.3 MB (2276372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245b496b9b8786da02acbc67cb5688327036e893326db970e4302e7298e0218c`  
		Last Modified: Wed, 24 Jun 2026 01:47:10 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-3-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a8420509108a219c32e64449ab853dd28d57ab52c6b8169756d787586dd2ba13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258052898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1583b722c6b72c570b59ca3500deccdd30f4cd6501258cb912411f72bd18d4fc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:50:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 24 Jun 2026 01:50:12 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:50:12 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:50:12 GMT
ENV JAVA_VERSION=28-ea+3
# Wed, 24 Jun 2026 01:50:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Jun 2026 01:50:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1167552c3864000b913ae25db6b6ebe6db4c02fb117dcf851ba7fd54e07420f`  
		Last Modified: Wed, 24 Jun 2026 01:50:33 GMT  
		Size: 2.3 MB (2314519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab51d00bd780817d6d225364192efe8f596570cd1504e7acc98184d36c68f3`  
		Last Modified: Wed, 24 Jun 2026 01:50:38 GMT  
		Size: 225.6 MB (225589828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:374ea6815f8ce50ce01f66c54ca8e8bd425f2a410ffa04ce52ba4bdd6c30b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952cc5da4a88c9e0789a7ea0e42193c3dbced6335b5f5a04442e2160040579f3`

```dockerfile
```

-	Layers:
	-	`sha256:7ac0ee907581cabdfeee6523e0c36c4fb0e5dc2549c6eb8a77da9eab1d45cc2d`  
		Last Modified: Wed, 24 Jun 2026 01:50:33 GMT  
		Size: 2.3 MB (2276050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c9e155c1c80e80bef595d5c447b4786b95e7a38cab9c18aa8f5b62dc7de75f`  
		Last Modified: Wed, 24 Jun 2026 01:50:33 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
