## `openjdk:23-ea-17-slim-bookworm`

```console
$ docker pull openjdk@sha256:90c711f21789eef8ef8d97e621b85543ff4659bec5217e2e6712c958b914fd5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-17-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0adeae2225722eec70b762b0c1ff59458b00e8d21078d2f06d7901118ecc6c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ae18e3b59d6a2e4d6988d90528e1f37e0d54d3760597dc613fd38985cced9e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Apr 2024 18:48:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005afe43eb8cae21091e569b6c3e0a85368332ff8d29a9732de89eb77432c5f2`  
		Last Modified: Wed, 10 Apr 2024 02:54:20 GMT  
		Size: 4.0 MB (4015025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad441cfaf4f47be38ac0dba1fcc77278ba890d7b20771665a0cd31d1b1e7b346`  
		Last Modified: Wed, 10 Apr 2024 02:54:23 GMT  
		Size: 211.0 MB (211007594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-17-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5eb0461de9e3bb58a9aea6fe9661ae9dcccfba54b60cf5f7ec1bbb06129b83ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1bf16b0a4ee54995f8aa7904a3029825652e2d3a07cd1f0e36570e207a7e82`

```dockerfile
```

-	Layers:
	-	`sha256:6f19f295235628dcaae6188fcfab63d6b43af894381090d86fb432951a8a7d61`  
		Last Modified: Wed, 10 Apr 2024 02:54:20 GMT  
		Size: 2.3 MB (2346220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb9cf82045a40c067df2e8e0f1732489b9533568508fe5c25193fb5f62e22d5`  
		Last Modified: Wed, 10 Apr 2024 02:54:20 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-17-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b63e481113380f23855fc85a0e6bb0f898d083ba9ac1d17c6a8c8e7e7a6b173a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241875317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1d83cb5964015201bf7c25240350ad3cd398f3c3b9e37ea6ebef679a019675`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63bd5c67700cc24a2dc61525fa979c1c1bf6d9931d1c89140c1658dc404a1d`  
		Last Modified: Sat, 16 Mar 2024 15:54:12 GMT  
		Size: 3.8 MB (3820092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4eab0228964c69967d6ecab16381d492efd1088b119acb875601a9f8c2839d`  
		Last Modified: Fri, 05 Apr 2024 17:58:50 GMT  
		Size: 208.9 MB (208898791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-17-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0ef4f4405edfe80ec77de3ee0125c84d2aa90e814c67f097a58e21491f326ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc300032b6c190005d5a52c0ae08b85cb83c87e87a696424b7061e404a30667`

```dockerfile
```

-	Layers:
	-	`sha256:543c808e8225b60287208a333b2774aa0a3185c0bde8e3b419a0dcfbd4184d62`  
		Last Modified: Fri, 05 Apr 2024 17:58:40 GMT  
		Size: 2.3 MB (2346772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080070ad34be18fce55e5df7e073d760a5998279be7f1789ba660e8bb245d9e7`  
		Last Modified: Fri, 05 Apr 2024 17:58:40 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
