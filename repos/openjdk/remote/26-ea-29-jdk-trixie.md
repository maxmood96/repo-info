## `openjdk:26-ea-29-jdk-trixie`

```console
$ docker pull openjdk@sha256:c1782ddacfacd31c601361ef226ce20ccd2eab664e53e954cb6c49ed3dc81720
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-29-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:8756fa6c315b5b4b4d6daaa87882b13a47321f94a7d72a1fac20d00a753896a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386701315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d8c08182c79ba39419d888890895b42478fbacb8272b246bcd99d7156d513f`
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
# Tue, 30 Dec 2025 02:43:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 30 Dec 2025 02:43:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:43:13 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:43:13 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 30 Dec 2025 02:43:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 02:43:13 GMT
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
	-	`sha256:b57ca17828e64af129a66a530a0ac861634e6408a6f842145fb4bd602fedbfd4`  
		Last Modified: Tue, 30 Dec 2025 02:43:57 GMT  
		Size: 228.0 MB (227957802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:c213916c0a0e8d0b50bee564997bf565fa750bc2ab2d97e32183c5af58da2aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80995b84582ad3ec76fbfdd8ee327b33783b2530241567384ca3dbf5d4243562`

```dockerfile
```

-	Layers:
	-	`sha256:dbec0b94b6004ccda7da100a9eb855ec362b68c7c50b5220992bbf19476420e6`  
		Last Modified: Tue, 30 Dec 2025 04:24:27 GMT  
		Size: 8.5 MB (8509979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5602bf97d6b2c49cda263ab1588579410c3e2ebec9c739014c09527447f179a`  
		Last Modified: Tue, 30 Dec 2025 04:24:28 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-29-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0cbf3a93d75d205915097f5c071f2bb3e3e1fc5f86a2402d1687b45038608c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384195751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a76be11b4735cca1a91a1ea7cb9f552670f6634b097f92de3f5efc0a0c4dab`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:42:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 30 Dec 2025 02:42:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:42:17 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:42:17 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 30 Dec 2025 02:42:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 02:42:17 GMT
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
	-	`sha256:235677f33825644032efc4e373ed405773e492fdbd9a914744b45fad72f4b66f`  
		Last Modified: Tue, 30 Dec 2025 02:42:55 GMT  
		Size: 16.1 MB (16071411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c00c4d5f4298bf3382d1e4c71dd4bdee7ea33fe27877a74e20dba78662dd18`  
		Last Modified: Tue, 30 Dec 2025 02:43:03 GMT  
		Size: 225.9 MB (225869318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0b5de43e358f2c06e03f30d9306b755d187f32ea8e9e777bc18cb9b06d88e21f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df148f8db4a7dac2c7ac7a8e50874077ca8e6cf9334eeb8d5ab009068a3d9d6`

```dockerfile
```

-	Layers:
	-	`sha256:07493175ade672c8f706661f1d434ff1acdb6520ad03e18337806c6313984ca5`  
		Last Modified: Tue, 30 Dec 2025 04:24:35 GMT  
		Size: 8.7 MB (8704769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18bc762d7baf447d684bccbdff354c1cfd0c164db3d74f519ac6c743c5a2298c`  
		Last Modified: Tue, 30 Dec 2025 04:24:36 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
