## `openjdk:25-ea-1-bullseye`

```console
$ docker pull openjdk@sha256:9918fb175f98e14006969c69e00c4fea5b7452780baa94703d190b8ba9a5bf5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-1-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:23d20fccf5c93fd3e762023e76ba3778645b091b29a3750cf2ad5c8dbf6ad563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351085616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f18dcb461287ffd8c23738d7fa8ec1cded764e60839176b660e819ecae6067`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6250b47f2f29032cd23422cf60c58f9b1292d8896e50adf93ca58b1f6726b6`  
		Last Modified: Mon, 09 Dec 2024 23:30:43 GMT  
		Size: 14.1 MB (14071419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86598476f21ad4cdfc0563d13017a85bd710e0414f7a5c00652ea2db617f0ede`  
		Last Modified: Mon, 09 Dec 2024 23:30:46 GMT  
		Size: 213.0 MB (212962691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-1-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:fd72d7be817c4490b37a8db6d8af2bcc131a00a0cf52660e0aad4fa74b24e591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8394593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5520ed9c24f2764ed570ac9505e5f159601908a5fd2d2adaab837683ac764085`

```dockerfile
```

-	Layers:
	-	`sha256:d86890e87ff5f20b7b463d315c87e1b8a0b53ff295ded4671490f7280b1f8dae`  
		Last Modified: Mon, 09 Dec 2024 23:30:42 GMT  
		Size: 8.4 MB (8375993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e7994326769ba704b221ef966d17de9ede269a95755398f3840b197f51fe3f0`  
		Last Modified: Mon, 09 Dec 2024 23:30:41 GMT  
		Size: 18.6 KB (18600 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-1-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:51c15a81d5c3e69550f2362ccf4c6cde13bb0b88343d57cd0fd2b0cd0a99cd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349081164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60d24d12e1311b589f62db9b68e4bbbd37f12b2f3837ac282b4476f76d1eae0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749caeb5baae1b5e6316a6f02e57835aa548497fba6792be844c743a57c72a2`  
		Last Modified: Tue, 03 Dec 2024 11:51:00 GMT  
		Size: 54.9 MB (54852316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72075f2e4bb2192408955026a169695446c09e734ec8d71fd14ded7b9b67ab5c`  
		Last Modified: Tue, 10 Dec 2024 01:30:44 GMT  
		Size: 15.5 MB (15526199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d9552bb3f1d7219f8d754e06d64cc5ee670db899d0568ca0b3f638ad14b5b0`  
		Last Modified: Tue, 10 Dec 2024 01:30:48 GMT  
		Size: 210.9 MB (210912607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-1-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:68748779f7b2e0fddb999acdb63768ab3b18e1a343e0b7b3cc73366910ce1af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8495821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd8826020620625ea5920f07495add958e702e792ba8ccaaddf59098591c56b`

```dockerfile
```

-	Layers:
	-	`sha256:41c4cf2539d0715ec4608d072029d700be08369847c7d941f63b28ebc5abba39`  
		Last Modified: Tue, 10 Dec 2024 01:30:43 GMT  
		Size: 8.5 MB (8477077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbb043f513db5e9affcbb51486e31be0d1bbd48ff3ad1b758a5f7980bd9d349`  
		Last Modified: Tue, 10 Dec 2024 01:30:43 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
