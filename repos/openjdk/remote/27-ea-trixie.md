## `openjdk:27-ea-trixie`

```console
$ docker pull openjdk@sha256:b9de8af764866a23d8b9e24687c78fb5c759b1065e888b1a03c27a1a3189ebc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:7aebd2eb7633b4bbd639a964fa970fc2c09996ef306249e138e85ddee12286e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385858509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c587e7c172fe067ea78943adcf86f264c291e0563931e76c5f18d312185071ca`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Jun 2026 20:06:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:06:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Jun 2026 20:06:08 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:06:08 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:06:08 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:06:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:06:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c090dd174892754543749072954d1b674eaf1b20c8c21452cd6c5f801a65c5f2`  
		Last Modified: Tue, 09 Jun 2026 20:06:34 GMT  
		Size: 16.1 MB (16065689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1310b8ee3015861cac8084d94c3e1a16f64687866c0bd0b251bb659db879433`  
		Last Modified: Tue, 09 Jun 2026 20:06:38 GMT  
		Size: 227.1 MB (227070550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:18ffca96a42eeb3ff4e06014ee255668653671c153afe94a97df86c949a1e5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768ed6c492a031683ae9085956dfbbffa47358d122bb2d49f6fc12a8086a138b`

```dockerfile
```

-	Layers:
	-	`sha256:b2b173da69779622dd473cd45324e7bd05360e2ad5bca3f4c9e9d011b329cd7f`  
		Last Modified: Tue, 09 Jun 2026 20:06:34 GMT  
		Size: 8.5 MB (8508787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890c5513375e893ffd1a47a97bb2622019b06ac840e773f3fcb22176ebef6f55`  
		Last Modified: Tue, 09 Jun 2026 20:06:33 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4d9cecddf271bc3820fa6fe54a921ae4acd02cb28fed3ef379a7c4a5e82d48d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.4 MB (383413885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbeb7c0ff7c86908a96aac021bf413173b4b2f612e616b92b370a970be7d0ca`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Jun 2026 20:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:05:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Jun 2026 20:05:44 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:05:44 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:05:44 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:05:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:05:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773fb68c2f06f95c711bde277bc0a35d5df3b6ac58ed1383b95eb19595b71cfb`  
		Last Modified: Tue, 09 Jun 2026 20:06:10 GMT  
		Size: 16.1 MB (16071377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f436ade9c50e4c9bcde22f2c033485ad32e522160859155d65799ef28c0273`  
		Last Modified: Tue, 09 Jun 2026 20:06:15 GMT  
		Size: 225.1 MB (225051833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:28099b56a35cafc1dac53c49327d6859f251da4bf37fc488bfdec99ce2d776af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8720972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2022193249a9b8efba27668f166cb04c13893f21827e861f2539bfede129f557`

```dockerfile
```

-	Layers:
	-	`sha256:f0052a16d698f39ce96895b81d0d69d3a62ebca837f1e13e66cab995d65a1d92`  
		Last Modified: Tue, 09 Jun 2026 20:06:10 GMT  
		Size: 8.7 MB (8702940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18c5f80ba9a61ba63a606e3418906093cd12453f0f2c3427eaec57cd8bc3147`  
		Last Modified: Tue, 09 Jun 2026 20:06:09 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
