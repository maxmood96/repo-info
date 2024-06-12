## `openjdk:24-ea-1-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:5cb4ef5708babf01645b9d7ad25a0cfe63b0bdce8c9cc3e20d2441127232cedb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-1-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:abf0e5a9484039ee35d2f6a23317f462fb88b85a3c11af345263b7937cfc029e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244314412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8acdbedb36f404cfa558ca8f6d0b290ff559335a5c8282251ec7521931f5896`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acedd10fdec50dd754199f31f040da17a3ea6eb3107c96fd942f87579ae8a69`  
		Last Modified: Wed, 12 Jun 2024 00:55:41 GMT  
		Size: 1.4 MB (1378105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08429d7b0409cd39d0e83462dcdb01f25750de16adc57c8419e66a21afdfe7e4`  
		Last Modified: Wed, 12 Jun 2024 00:55:46 GMT  
		Size: 211.5 MB (211502376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-1-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:75da37602e9f55ec936e3c839d582037853736377d6f79baaeb89e084cb9de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283f6733d45f38c5f2b7bd54c1273e8f3e8590696533e9c93c6b9a480fc6867b`

```dockerfile
```

-	Layers:
	-	`sha256:802b69dd74502acd18eb815f70a2067a83527ada81b7c832aa17b20e328591b3`  
		Last Modified: Wed, 12 Jun 2024 00:55:41 GMT  
		Size: 2.6 MB (2638484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e17f1b525055550589bfdaf1033bb6932c32138884c453e94272098396a199`  
		Last Modified: Wed, 12 Jun 2024 00:55:41 GMT  
		Size: 17.3 KB (17344 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-1-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:40e12c81f2c31eef804399101e93ac12623e08bde3ac6925f5a25e6b365b4b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240831378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66276c7d0d0ec450ba5c3f959e80b86bcdec4d39b0ca0a991289fb5421460ee`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48635aa3a72f5d9eda6c04795e37ca650ed83de84a321f1dfcf864eb7780709`  
		Last Modified: Tue, 04 Jun 2024 13:50:07 GMT  
		Size: 1.4 MB (1361913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71962f922baf196b91e902156013b308bb7f6b67e27e99d8e1dd8cc14f170f7d`  
		Last Modified: Wed, 12 Jun 2024 01:51:49 GMT  
		Size: 209.4 MB (209382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-1-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0d9b37cbe0f48912bdc32bc36ce3d64f6ddd1a46b24b89771cc5d1ff8f1f69d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04ea69efe6a6de99e446354aa62ab89cbd8d5934724ba0bd6c24689feac7d4b`

```dockerfile
```

-	Layers:
	-	`sha256:adcd3d37241b83344ac0038c0bc0ed13adfd7e1eec8e150f2995742c2489a24b`  
		Last Modified: Wed, 12 Jun 2024 01:51:45 GMT  
		Size: 2.6 MB (2638760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d1d6d0c06321f99bfabeda57cee193b87461eef786393420d2cd53fa05ab75`  
		Last Modified: Wed, 12 Jun 2024 01:51:45 GMT  
		Size: 17.7 KB (17678 bytes)  
		MIME: application/vnd.in-toto+json
