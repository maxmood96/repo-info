## `openjdk:25-rc-trixie`

```console
$ docker pull openjdk@sha256:1e99a3e6da32ed2a73e0c3d6320fdf18f78d46d7fef7a4aec46f2151635da4c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:146a6561773d0d7ecb6b1a88c0b4984096ec6c7f1ec36f52313c952e8128ce9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381918473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8223b23ed7435d5d8f33350306cd20448424bb6ee4c91f9422facca029b6b1a9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7359303b191828ad8b3feba05420384bc307a6a7a3c75a106261e4e2391c151`  
		Last Modified: Mon, 18 Aug 2025 18:16:41 GMT  
		Size: 16.1 MB (16061373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea559d0b9b4923892c6e4a85245a5dcb29801f011885c96687e09857e82c4431`  
		Last Modified: Mon, 18 Aug 2025 21:32:01 GMT  
		Size: 223.2 MB (223188564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:f8cd9cb893f4337b19082df5b268f951108fdb5a603b2eb08f17c340d5bde05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd52b380ff8d104d7a602da5a0eb3e2fb623c5f60a2878d64e27d61ea4d61af`

```dockerfile
```

-	Layers:
	-	`sha256:ab94ea4d64ecea0204cbaae82188309bc8bcfc2921310283f093b667eea48403`  
		Last Modified: Mon, 18 Aug 2025 21:23:56 GMT  
		Size: 8.5 MB (8508322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:399f8feb4a9f673428a3bb15d8b51f65859a9e2a504c7e23ffd010668eb2f03c`  
		Last Modified: Mon, 18 Aug 2025 21:23:57 GMT  
		Size: 18.0 KB (18003 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:edbfca3ad8fe8c194e934864775fbb628e361a8d9b8c6c005fd5b7d9daef9bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379306011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a623ac1b414212129ede019a62f7f4d792a4810c8b350e723a5c1883204679a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e07437b7d82281aa4925b53bf361031ee6dcd0a4c9dc36ebd8b5e912feabc18`  
		Last Modified: Mon, 18 Aug 2025 22:23:06 GMT  
		Size: 16.1 MB (16070603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b681373d3c2f453b037cbdaf0fc8f34400554ffc065961272f81bb9e2b5fb37e`  
		Last Modified: Mon, 18 Aug 2025 22:35:33 GMT  
		Size: 221.0 MB (220985567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:7e42ecb261a9b0c3579bf219cd0259fb5517c978fca9cfe0652972c194be63f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c210e604b152cb0946d02d385143ee1dad0d8abe90dcf580febf52896d6e29`

```dockerfile
```

-	Layers:
	-	`sha256:bd0d8a180fe8d4e62c853ffa7d3e36bb26ed9d0df06a0aaeab7056105410b98f`  
		Last Modified: Tue, 19 Aug 2025 00:24:05 GMT  
		Size: 8.7 MB (8703112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f340cc0adce1de23f1592b7feab9ce692c621a8129296aa65c0513fe859033ba`  
		Last Modified: Tue, 19 Aug 2025 00:24:06 GMT  
		Size: 18.1 KB (18122 bytes)  
		MIME: application/vnd.in-toto+json
