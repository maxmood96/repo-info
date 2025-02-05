## `openjdk:24-ea-35-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:4b61246b276f819b6d2c1840bfc5e5314497c0f3e21b40b408bba8c1247c6a3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-35-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:bd1863f4f95878f8fb3f23fef1796ec1be43bf79d2e91114b2c83a6f4770ab79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244630945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac4fea2a91155a003ea9f9309587cce8a787fa8f502d30cfee7f69796d30756`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bc762dc1b85685566b1f7a2bebff998be80dd366d697df1bb184d211530587`  
		Last Modified: Tue, 04 Feb 2025 23:32:34 GMT  
		Size: 1.4 MB (1377233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b12a028ae9f2c8ba018a67c9fb19f8eb5b4a556d11f6b64366829cbd3b0a6f`  
		Last Modified: Tue, 04 Feb 2025 23:32:40 GMT  
		Size: 213.0 MB (213001124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-35-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:26a8e1de59208b83d5668c655e102f446f9aad28a98884f8b3350cc713c77c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3808da4a7aad698dc93e739cf530d64140d51168cf8f2b365d39cecd0321b8c7`

```dockerfile
```

-	Layers:
	-	`sha256:466bcb849a0c5f7f5e7064c39a0b77d1331aad8c2e4426693f52e2be3bbd6d9b`  
		Last Modified: Tue, 04 Feb 2025 23:32:35 GMT  
		Size: 2.8 MB (2831682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883adadb805bbf5e45de109a09b4b97638a8726ce1b9151a264e26e3e36f1919`  
		Last Modified: Tue, 04 Feb 2025 23:32:34 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json
