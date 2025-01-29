## `openjdk:24-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:920f52276d2e8a28efa8a817dfcbc64a61d752f7f33aa48e3f39c82ae45269d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f092f47e86b817816abe925bfca336c8c12cadbfc52544f8f599bc0abeb5b189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245176233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc29d13c6d94e764136222d9d87295d84ba5d4848a6987cac174969b6aa888b7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904849acc590b27ce6e1760c4b02ab9be92f7b520f1f0fc146bcac640767221e`  
		Last Modified: Tue, 28 Jan 2025 23:28:12 GMT  
		Size: 4.0 MB (4018386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64e1a07cede1b62c29a9b7597db3210946ef5a4208dcbd0983e825ebda7fedd`  
		Last Modified: Tue, 28 Jan 2025 23:28:15 GMT  
		Size: 212.9 MB (212945430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:985102db496916ffa11a3aae17c56800b06e6f18cfac99b763fe6717dc464f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d2afd67f5181fe6da519f23ddba368bd2651adbe2e55087523c96201306dd8`

```dockerfile
```

-	Layers:
	-	`sha256:81d47a2951bd5ff410c2709b69ed68e7e82af08b89c9f15bfb5e13052912a784`  
		Last Modified: Tue, 28 Jan 2025 23:28:12 GMT  
		Size: 2.5 MB (2534519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81cb84ef6fdc4a3d3c7128732da99a37c0674da966fb31e34fe7c1edb01d819`  
		Last Modified: Tue, 28 Jan 2025 23:28:12 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:03d2ffd6f11ac8b4e1e861f59869a9307a4aa4b4c15215f7c657ad44abd7183e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242779647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf311728e0db342295470853130c42ebfc33c4d29ac5441cba9e44e182c0520`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f083f07e13bd63cd44a785caf631d4e023799e01a18898c1a673879d76b06aa`  
		Last Modified: Wed, 22 Jan 2025 02:34:57 GMT  
		Size: 3.8 MB (3833715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5861a94b5957723ebe62a87b80997d7c9b1372d3847ba10af22edbb2581aa89`  
		Last Modified: Tue, 28 Jan 2025 23:40:39 GMT  
		Size: 210.9 MB (210904901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e1cbacc3ee8ab4550879cdeb18331624956a0f52f2e09bbf9194c758dc01fc49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ef4c7fa954f170692a88d1c397c4a93be5fbfaefd8773f362318912e1eaa81`

```dockerfile
```

-	Layers:
	-	`sha256:8be96df466f3af17e9fbba098948955bdf35941dfe66bff004fa6f555f50c712`  
		Last Modified: Tue, 28 Jan 2025 23:40:34 GMT  
		Size: 2.5 MB (2534249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0792035d11d2c6717db71861edca4866b96f234d0c202ed643824b12148752f`  
		Last Modified: Tue, 28 Jan 2025 23:40:33 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
