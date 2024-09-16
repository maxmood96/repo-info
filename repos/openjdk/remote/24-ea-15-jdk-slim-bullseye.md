## `openjdk:24-ea-15-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:540b3d0cd13fdfdd0ad64941adabb2b4aa5cdcd5664991e4bc55a169524861e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-15-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f5529dfa80f9b7550356e4b1cd53fbdf15f31a08c1f97d8b7a4f804ee79d10c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241506743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed124fa7a47cc0e042b20b456bae2816a6aadbbe1d6869f294752af3364fae0f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809d4cf587258fee9a9ec125bc8bab03389c801bbe5e1f5d0a27c27746ba882e`  
		Last Modified: Mon, 16 Sep 2024 19:26:19 GMT  
		Size: 1.6 MB (1565908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba8cc3e631830b7a75add8726d62e649c389a0641cb10631fd6cb56fee1a3d7`  
		Last Modified: Mon, 16 Sep 2024 19:26:25 GMT  
		Size: 209.9 MB (209866470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-15-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:10d4ffba64ce9da7bc2f288b1df9f057c71730bb94e12109429fa80d355ec15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2ec53ab4df0402937259a3e7eaef6203f04edee2f0e80bd08876c7dd9d348d`

```dockerfile
```

-	Layers:
	-	`sha256:856109a4a5414064cfbcc47ce478769ffc2c058e57a5cc328bd452988328532c`  
		Last Modified: Mon, 16 Sep 2024 19:26:19 GMT  
		Size: 2.7 MB (2659450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53248abfd3d5f18e9973ed27112327fa0d03596975880d98236d07a2aab9fc9a`  
		Last Modified: Mon, 16 Sep 2024 19:26:19 GMT  
		Size: 17.7 KB (17690 bytes)  
		MIME: application/vnd.in-toto+json
