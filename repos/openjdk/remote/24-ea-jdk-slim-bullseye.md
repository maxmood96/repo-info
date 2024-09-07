## `openjdk:24-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:7b0e99e0133fa35a8b1bf7d1e412debf7581580bd405a775e0ea0820d4fb6337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3755af9f95f033aa73828cd7b61f8c75e320b88e0659c8a6926661239585a69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245015499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab067554d0e69cd0014a306c6df7a63b69ded0c7d09681ab0685cbbeaed7738`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Aug 2024 18:48:14 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 29 Aug 2024 18:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6ff78227fb6865113ff0e844c0e3dbbd3c3fee0fd03b4a3b3f7134390f785bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='21518bb62faf883eff4bfb1e2c69a5b50d6b3e96b30b0a111f1d1f41a4205fae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d468ba5404897e81269667302cf4cefc3baa32d1c0b00b8467a66e95ce11d6`  
		Last Modified: Wed, 04 Sep 2024 23:11:31 GMT  
		Size: 1.6 MB (1581809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac85c3f022fc4a2a5945e7c1bacbcb79561e7b30dfa79b6740be247f087d4bd`  
		Last Modified: Wed, 04 Sep 2024 23:11:34 GMT  
		Size: 212.0 MB (212005013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e737fb0c869b336a44809520de5fb2219dc555009e3a0dd2d6b6749dc3539401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2676532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1689aa201a4df31d07ec4ab8e8af0c7e636f4c17876b3b3a5fc0f63e1d0a417e`

```dockerfile
```

-	Layers:
	-	`sha256:ccaba644064041d2921ee03247b8315ded5026ec4e1391c3e9cd30e8d6001efc`  
		Last Modified: Wed, 04 Sep 2024 23:11:31 GMT  
		Size: 2.7 MB (2659174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c396c2444651bc2706f0d7982e7ebd5bb1ace5c8c8f3c990501c692d51a143d6`  
		Last Modified: Wed, 04 Sep 2024 23:11:30 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4c95a56532ea092f92395c72419d40fda343e9b7d84093b1bd6567de39f46a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241479794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3412fc80b9fd48347231c9ff9d1d5fb164527aefc5c818c235e3ab5d03350174`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f77a56007489f879acbedc5b5e52a29d353b488a053f996aff119c57226030`  
		Last Modified: Fri, 06 Sep 2024 22:30:57 GMT  
		Size: 1.6 MB (1565885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf3dfa341aa95951a901ece84d3d16de0cccbd47466b054a0f7c466eed52cc0`  
		Last Modified: Fri, 06 Sep 2024 22:31:02 GMT  
		Size: 209.8 MB (209839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:22319920d53aeb6643887bd80b54d740593c287f6685b16bf40c380919ce271f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd888bafbbfcce38cd13b631b12ea68d2c711acdb90cf5b45189f924f3ec40f`

```dockerfile
```

-	Layers:
	-	`sha256:fa2ee94b79cd97d9fc54429d318454c6baeb520716d006f5e9b52e5180a79f8a`  
		Last Modified: Fri, 06 Sep 2024 22:30:57 GMT  
		Size: 2.7 MB (2659450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2026e92b30b3d5d4f0935a089db27ddd55b27cb0b38e88060010cde343bd8c58`  
		Last Modified: Fri, 06 Sep 2024 22:30:56 GMT  
		Size: 17.7 KB (17690 bytes)  
		MIME: application/vnd.in-toto+json
