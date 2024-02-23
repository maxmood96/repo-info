## `openjdk:23-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:2c6d9da520721295bc7683e247e3a30cb55aa2dd4985ee0b389b6ab757b21156
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:26571ee1f2e9ddd6c99387802226819d9d8829d3631ed49922fbb8f45139e4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236272375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf5e95c0d57c779241dc02b776d139c4a3be36da2a8b3dceff99d7bdb815cfd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=C.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7caab80e91771595a094b2b4b3f818e043b083b971331e1e668211970c6589c`  
		Last Modified: Fri, 23 Feb 2024 18:51:09 GMT  
		Size: 1.6 MB (1581764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a0f2636ee98d718cda30433c67c92987d272ac9b218fe469545162c5fb65`  
		Last Modified: Fri, 23 Feb 2024 18:51:13 GMT  
		Size: 203.3 MB (203268186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5972ad7c800c0af52df65fd795aa81a1ddb4e9b63b1d43e61e9ef44f829754c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4f9c1440af574f83aa8a73d5600aa2394faa2ff7996f23d10657c7c5eaacce`

```dockerfile
```

-	Layers:
	-	`sha256:9073fa458e03e562dff2b2f3968d870946fd5d2cef30825a4e387f7113e0b0b3`  
		Last Modified: Fri, 23 Feb 2024 18:51:09 GMT  
		Size: 2.6 MB (2638332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fd8c93c474492266e375d40a70aedf4ec2bcbe4f81d5ba04dfabaa90b526b90`  
		Last Modified: Fri, 23 Feb 2024 18:51:09 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dd4a4b6a36c04073704c4409c1ecbb9f1c2f8405dea34f364304c83b8e5cef31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232803064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303abd32ebdbddb3304ef54002ab6875826e2b7308d9f59a43c8eb0974b6774a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=C.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66665e7107836c004c0e092f793e4525c11b530024a61f362798cc6f7500ab93`  
		Last Modified: Wed, 14 Feb 2024 01:18:12 GMT  
		Size: 1.6 MB (1565944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ea763655687d328f2e1f01c8f54b799a99d06f207c38d7fa6fcdd77d57796c`  
		Last Modified: Fri, 23 Feb 2024 19:07:04 GMT  
		Size: 201.2 MB (201166043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a04eb793f5c26fcb858cf728cd8b3f1262be4eac47cbc8eb0319a3e8808cbb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652025fe6c6149b121cfd241137354016aa6e0f5dd7df81bf3c538074d13dd15`

```dockerfile
```

-	Layers:
	-	`sha256:bb3941525cc9e26bbb8ba97f1de25e9c5c2b1a3d4dd2b43f073ac4452f560848`  
		Last Modified: Fri, 23 Feb 2024 19:06:37 GMT  
		Size: 2.6 MB (2637586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa8664274d693eca495d11fec700f8236a4db4623ffab044179aac8749f8f25`  
		Last Modified: Fri, 23 Feb 2024 19:06:36 GMT  
		Size: 17.3 KB (17318 bytes)  
		MIME: application/vnd.in-toto+json
