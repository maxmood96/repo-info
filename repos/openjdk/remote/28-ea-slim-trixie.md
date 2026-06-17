## `openjdk:28-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:f176973a36db4b7acd7b1b14b42fb7f28ffc3932ee7d6b1500f292783a9a53fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:c872271244fe32f7f89155e287213b480324bf827249a26704a82ab6c864b9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259705025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a464cc4b874caf9e87534a5e6d9242fba54fdb2e5f15e1393dacef633bb6d9c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Tue, 16 Jun 2026 23:32:24 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:24 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:24 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf245919bfa8a264c446903baa10ecf155c960dd5079af1b817053169947078b`  
		Last Modified: Tue, 16 Jun 2026 23:32:44 GMT  
		Size: 2.4 MB (2371316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b4913b858104de6c0898795ae7d406c60e746a347fc43e43c901a0c7c7a3c3`  
		Last Modified: Tue, 16 Jun 2026 23:32:49 GMT  
		Size: 227.5 MB (227548294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:15597974be9cbe9319185526ebf224ebf449ab4916909b9bf8a12fb991d5032b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0902064122619d02fe0ee8fec8a4cd8821b419357291a13914204d44e9c52ff9`

```dockerfile
```

-	Layers:
	-	`sha256:d684440dbbb4fdcc68019beead6c221c1910f117c4a2f0e44fc7880b114db071`  
		Last Modified: Tue, 16 Jun 2026 23:32:44 GMT  
		Size: 2.3 MB (2276370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a80d63bd908aff470e30daaa2fe20f598dcde12e54905d1c2a5d7d7ab617ad1`  
		Last Modified: Tue, 16 Jun 2026 23:32:44 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ff348ab40cd8cbc5e2a5df7e7d52f04dbc656b6ade65be97a81538241689a143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258039086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a6bbc8c1655b8d882be854c21fd3928add031501109353441883652827c3a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Tue, 16 Jun 2026 23:32:14 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:14 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42106bc9236c680a791db3bc3add359a60656d67f92ba77a5bccf1e273cee034`  
		Last Modified: Tue, 16 Jun 2026 23:32:35 GMT  
		Size: 2.3 MB (2314524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4723dd14f72d4a39f4204d2a8950feeba902ea3b20056eb7c984fd896a66ef`  
		Last Modified: Tue, 16 Jun 2026 23:32:40 GMT  
		Size: 225.6 MB (225576032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ccc4b9e3a17196fe0084b788666e442a44f9c969c460e0ce16b70eebbca27c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c2fcf3a441de648959cf9913279d4ba0f1adc675c2bfe4064fd2863d58a313`

```dockerfile
```

-	Layers:
	-	`sha256:b213d4fe9f16835d9cff4ad0854c43f91112e5d4b9e500b3a4d7bdb074dac883`  
		Last Modified: Tue, 16 Jun 2026 23:32:35 GMT  
		Size: 2.3 MB (2276048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4acc1d29f02d53a171b54a14e3ca7fe1bdda79bf5586df8c7f359a954d76e815`  
		Last Modified: Tue, 16 Jun 2026 23:32:35 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
