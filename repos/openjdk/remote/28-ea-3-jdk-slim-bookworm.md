## `openjdk:28-ea-3-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:8dff6be73caa83a00c9ad932179e4e3dbe11f0d4b54accc73f98a3e389f27880
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-3-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:fffbf990bb318c87ba9052d3d9db7a900691dda9d407e41f1c0cdcf61c38f023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259820377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cfc03184f2e63869555588734288b39c4e8d742ca7d72f44b4b15ac71351be`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Mon, 22 Jun 2026 22:38:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Mon, 22 Jun 2026 22:38:49 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:49 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:49 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:38:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0eecd324100b290092896bd8a36a624eebbdac38be4b3fdb6b175d40e8fa4b`  
		Last Modified: Mon, 22 Jun 2026 22:39:09 GMT  
		Size: 4.0 MB (4032951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b2d5c5a85d8740b2b6baac8214ece2632b7254e9cbef0421c11074da7d205`  
		Last Modified: Mon, 22 Jun 2026 22:39:14 GMT  
		Size: 227.5 MB (227549802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:79fbbfc44f864f49f2149c3f002ea7b3ea53a72091b8864d5aab2d1d3055033f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b5a697b999b017ab1bd0273b7a4c7e101aed7f1a81720b6e8dd5e2e07cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:27f61936bde3d33b5d8c6dc3f0d8372b749fdae18965f7aeb77b88426a71c251`  
		Last Modified: Mon, 22 Jun 2026 22:39:09 GMT  
		Size: 2.6 MB (2647282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2992ae78778c710b4ab51c95ecc5538920dfd9cfdec43a7b062a49fba30f9e25`  
		Last Modified: Mon, 22 Jun 2026 22:39:09 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-3-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b3ade8d8957268a9e03ef723e3c32d6757adc7b386fc24e280ae09e2b47edda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257563763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef89d73c32ccd48482cadae1ef4de6d1363901f73b3bbced52975061387b867`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Mon, 22 Jun 2026 22:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Mon, 22 Jun 2026 22:38:49 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:49 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:49 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:38:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70ee7a980c839c9ae4825ec53149143b4f13fa48727f006a54a68045d5f711a`  
		Last Modified: Mon, 22 Jun 2026 22:39:09 GMT  
		Size: 3.9 MB (3852804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd349ab9d8921d6da0a33ac57501c26e6a7f1eb1b470c1fd8ee6504578a49a26`  
		Last Modified: Mon, 22 Jun 2026 22:39:14 GMT  
		Size: 225.6 MB (225588652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:951d2a7c20812857ae75d2228286d8180adba03b1639193dae7af7b642fe047b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8115377b480deaf001d3dceaa1e5242776a1017cf9b4944a4d9fb977dcf6b60`

```dockerfile
```

-	Layers:
	-	`sha256:f9f86afdb2d5637c6c1c62094f69b9e6b1839337e6bc991fb09af19422af4044`  
		Last Modified: Mon, 22 Jun 2026 22:39:09 GMT  
		Size: 2.6 MB (2646916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d278415ec72be2d36e664c07338116bea78a312da3007ec2c46d20146e8c3e`  
		Last Modified: Mon, 22 Jun 2026 22:39:09 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
