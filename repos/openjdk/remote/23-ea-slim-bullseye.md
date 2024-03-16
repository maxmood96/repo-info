## `openjdk:23-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:e1b4e4b959543cae65b6d557a2438e8f99b0b9ae3d9f8491ac145ceef071251f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a7ec42096f4eedb783c7be428b25c3a11d5fdb090b2ec6c41aa4c383d44a3965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235932798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8dfeb46496e7f160bce04002fdc49c070927f77f89e9034dda81db4393daf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Mar 2024 00:48:42 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 00:48:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160ea70ce88c829ef4b9e6575341816ab3a5168f4a2bc3872989d0c528feb5e8`  
		Last Modified: Fri, 15 Mar 2024 23:56:04 GMT  
		Size: 1.6 MB (1581854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395d598e54615ddd4b8366562c36250eabb2edb7be143058ba650618306f44bf`  
		Last Modified: Fri, 15 Mar 2024 23:56:08 GMT  
		Size: 202.9 MB (202928455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bd740b26412df6020c5f56a4f1ab904e2feda88d2945083b97f4c0c51b1cbf8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a656a492d182d5a30a8e816c2b86b4ec52d590d7003967e87846255712b4d174`

```dockerfile
```

-	Layers:
	-	`sha256:f68d2b6abf55e4a2311363a61a8562fcb75b137e237d611a9d120a742f90eb9a`  
		Last Modified: Fri, 15 Mar 2024 23:56:04 GMT  
		Size: 2.6 MB (2638334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67379ac15c469a2a77ee0571a3ef73d2565f8c2aad78ca7f7a7154c424db1c1b`  
		Last Modified: Fri, 15 Mar 2024 23:56:03 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a55d634c9761dac04e35e59a27f5b4986fe8f7b571fc180cb963d0af96b671e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232427521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e30b5cd4b9bf762cce21c32baabcda061f74761f4099e5fedbb92a0f95d6300`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Mar 2024 00:48:42 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 00:48:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a999e7ea0713e0f70812c73c3a44d4933028059c0e0e95008ffb99319b0d52`  
		Last Modified: Sat, 16 Mar 2024 15:56:11 GMT  
		Size: 1.6 MB (1565943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6dfc668ea6644149f9eaebb18902eac7d3bc541dab214e22b6cb57d37a545d`  
		Last Modified: Sat, 16 Mar 2024 15:56:15 GMT  
		Size: 200.8 MB (200790462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3d3d0231aae85c92ff32e7e9ae0309f05f5ca93d963d2120f609ba108d7ddd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b122268fe6a2a2697acb8bcde6110eaad3a4440b90e26b3973edb9b5bd9c8587`

```dockerfile
```

-	Layers:
	-	`sha256:f0dfa1fbfe994326946eda98ab54f9fb6792609dd7e033d51041f043734db3a3`  
		Last Modified: Sat, 16 Mar 2024 15:56:11 GMT  
		Size: 2.6 MB (2637586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50849e72e8d963707381bf551288e91b754a8cc9bc6151cc8f397d1fb115d7d8`  
		Last Modified: Sat, 16 Mar 2024 15:56:10 GMT  
		Size: 17.5 KB (17486 bytes)  
		MIME: application/vnd.in-toto+json
