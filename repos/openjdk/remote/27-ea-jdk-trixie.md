## `openjdk:27-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:c0964d6507f6d7818651933357c7c7a8a4c6865f9fcd7aa7bffa4c795cc66266
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:2954a0f69275b09c51fb2d8d16b3a4c01067456f281bfc4d51460331739e1a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386798370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca43d29b6954bc0c680c7f163405d5223ef80a0bb4975d6ed73dd19619f13067`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:44:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 30 Dec 2025 02:44:15 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:44:15 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:44:15 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 30 Dec 2025 02:44:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 02:44:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38570246981f82b392055dee3e3d267ee2a135ab5f8cf64061fce4c8afe8e309`  
		Last Modified: Tue, 30 Dec 2025 02:43:51 GMT  
		Size: 16.1 MB (16062704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5be8e7c6674471f8a6464034913100a39f2be3cfe01fabdb003b17f18c9cf5a`  
		Last Modified: Tue, 30 Dec 2025 02:45:19 GMT  
		Size: 228.1 MB (228054857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:f8a183b1f6b950f1c7282a3edd42f196a752dbdb60f382f5b69ee3460d0b04ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26064adb76bc176c3c1e21aee52a44d1dacfee346189502a01f5953cd5aa67a4`

```dockerfile
```

-	Layers:
	-	`sha256:cde0f4396996d09d56084ffca94a0a35bb733d2d56a53f2eda58d50633bda420`  
		Last Modified: Tue, 30 Dec 2025 04:25:43 GMT  
		Size: 8.5 MB (8509971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58775ccc9d0e3fdfc6856146d8a116903d497f371aca29110fbcbbbcd9a3d54`  
		Last Modified: Tue, 30 Dec 2025 04:25:44 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:20adb79104537aaea13bd4b60868c185c98f81a091e9cc91b78fb4de8014333b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384298061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f3dbcb2b17c5f0e1f607a74c7ad0e855a89384f9221c2a902b4da47c491053`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:43:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:43:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 30 Dec 2025 02:43:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:43:41 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:43:41 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 30 Dec 2025 02:43:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 02:43:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b0e9b1859ce323409344b51e882db4fbe7dfb2d755d9a7df55af123ee75872`  
		Last Modified: Tue, 30 Dec 2025 02:44:17 GMT  
		Size: 16.1 MB (16071369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d91c43831168589b9eb865b7584c2c0a7cf27384cbffe85cf958b4f041f28e`  
		Last Modified: Tue, 30 Dec 2025 02:44:26 GMT  
		Size: 226.0 MB (225971670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0bf3f8f5374ee6b3864241994159c7c49268aa6ef70b61f14f6a9617108a10af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d91086747e13c68c822dd30661c6923eb67918c7813a77e4c9b1c22d41952f`

```dockerfile
```

-	Layers:
	-	`sha256:123f7834f383cedacbf8cb134a6e3a81d4913631abc15fcf65f0415cd3308c4f`  
		Last Modified: Tue, 30 Dec 2025 04:25:51 GMT  
		Size: 8.7 MB (8704761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a069cff6bb450197b46da8fdb7d9da8a1de32d87598e84ea78eb807911d462`  
		Last Modified: Tue, 30 Dec 2025 04:25:52 GMT  
		Size: 18.0 KB (18014 bytes)  
		MIME: application/vnd.in-toto+json
