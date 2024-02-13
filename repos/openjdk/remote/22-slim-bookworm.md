## `openjdk:22-slim-bookworm`

```console
$ docker pull openjdk@sha256:f4c1020867a545b54da5b75664405873c6dc84f5593ff7f64eda4fb9843e2775
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:80a97db3de5204045d84cc6c4e75ba1ef122de58d0e3758af49d6e1f99b2e823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236070726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ce8c16bf211f2ae9fc8bddf1680734d11a34fe1ca97e71250900901e9957ca`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Feb 2024 19:48:12 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3948154ac86ae3ac137ec921211ecefc8e0a451060b48efe9164c85530b6ca91`  
		Last Modified: Tue, 13 Feb 2024 01:54:03 GMT  
		Size: 4.0 MB (4015032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83c5a3ddd7574deb54857d327c718518ecff85e41cfce609ca4e552352b9f42`  
		Last Modified: Tue, 13 Feb 2024 01:54:07 GMT  
		Size: 202.9 MB (202931603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2f5bab6e952ca456b77bd08d3c31d97d09c0498cab160d04e7aceb3b9083c422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc80f738a82020f2017cc7817cf0067ba5dccfa7f49c6e8ffcd1f5900cb4a31`

```dockerfile
```

-	Layers:
	-	`sha256:65b4ad64abd1d9d14f02fdc6a392d2ac8d9c82c073c97dffca1141dfe8f3123d`  
		Last Modified: Tue, 13 Feb 2024 01:54:03 GMT  
		Size: 2.0 MB (2035922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:808490b02650f7d45aa72353640d962fba47a3bc9e86cd088495cbe5ff1e01d6`  
		Last Modified: Tue, 13 Feb 2024 01:54:03 GMT  
		Size: 18.1 KB (18104 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ab2ff3a39d7671be7bf50c05f24db99c853bb616001dbded3c3cafa3fb95dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233795262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c967c20aa8cbf115b3cfd59dababc903d742189efab0f986f463bfbfef06f80b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb8efefdc6916139a6831cad4526d3f8a27ec25946cb6e74ad7b0f0beaf36d8`  
		Last Modified: Thu, 01 Feb 2024 16:20:11 GMT  
		Size: 3.6 MB (3629642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16c6487466d1cad70c09d7b7c4130e9a7a41d4a60fb948affe5ab0b913b9982`  
		Last Modified: Tue, 13 Feb 2024 00:33:38 GMT  
		Size: 201.0 MB (200984788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fb2e8303c35cb02cab73dfa2b36d26b3e128223debad944afe90b223bfe826f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39773820fb6cf0724fc865e69001fe8c4388c6f3f8cb07b80251480b5aae8b5f`

```dockerfile
```

-	Layers:
	-	`sha256:232ce437efe4487cf01ee4ead74d7cbffa483f213a10aba2f3429cbefaed27b4`  
		Last Modified: Tue, 13 Feb 2024 00:33:33 GMT  
		Size: 2.0 MB (2036201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e7a69747638e51a4a6f1f67be710ffbe1bf52a29b14eb6b4f7c38b854ec44b`  
		Last Modified: Tue, 13 Feb 2024 00:33:33 GMT  
		Size: 18.0 KB (17954 bytes)  
		MIME: application/vnd.in-toto+json
