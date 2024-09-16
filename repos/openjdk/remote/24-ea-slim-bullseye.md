## `openjdk:24-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:955bfef8cc43d7ead89c93a0d9fb30a80a9277fbef6ba072f02400c4638b22ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:7e32068695d9fcc513492d706ffb324654af10972dd03b3709791917a42f695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245008958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d96d9c1d9bda1d38178e0408cfd0bb11b80aacfade16c40e62385e5154bc413`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
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
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87a164f77d9b151b90773780cb352a4f0405a753a7bee3a3afe148ca72c5ac6`  
		Last Modified: Fri, 06 Sep 2024 22:00:54 GMT  
		Size: 1.6 MB (1581825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51dad288dc992bc6d3d75ef5cf3dfb8342f31c0d1f911a4aa9b628634c6033`  
		Last Modified: Fri, 06 Sep 2024 22:00:57 GMT  
		Size: 212.0 MB (211998456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:74fdbb7bafa723542194c7ba675fc20761343b629ce86d429ebd7cbe6f8a40f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2676531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b3ebc92cfbecfbe7973db31f74558d818fb47cae1073b14f8b60ea327efd2e`

```dockerfile
```

-	Layers:
	-	`sha256:e99b4172e774879a0093e64aae6637fea021fc3c0e88a026e068efd323c3eb5b`  
		Last Modified: Fri, 06 Sep 2024 22:00:54 GMT  
		Size: 2.7 MB (2659174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b2e2077ab7aac37d19850259d7f60d5f683899f9d189d0a2c58f7d9e1e840c`  
		Last Modified: Fri, 06 Sep 2024 22:00:54 GMT  
		Size: 17.4 KB (17357 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bullseye` - linux; arm64 variant v8

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

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

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
