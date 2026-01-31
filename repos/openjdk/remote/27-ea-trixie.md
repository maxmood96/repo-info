## `openjdk:27-ea-trixie`

```console
$ docker pull openjdk@sha256:2b83ef39266fc25d11ee4f0daba399ec7b6fbd4a230abc660060151922140da0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:72a00301f30029722fd710befb444fc04636261832853a334366dfe7bc6eef96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.1 MB (387111702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5961fc40a8411fefb9734a24c7730621748e28fa7371905cf937ef8ab96435`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 30 Jan 2026 23:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 30 Jan 2026 23:40:32 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:32 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:32 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e33db17f9e97ad22a8aa23b2c581fd5cfb04727e545dd58e69c7d140abfb19`  
		Last Modified: Fri, 30 Jan 2026 23:40:57 GMT  
		Size: 16.1 MB (16062899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d79a9c948370d007499d45f4d119eb0d87c91bf265b935d078764e1ccf4b2d`  
		Last Modified: Fri, 30 Jan 2026 23:41:01 GMT  
		Size: 228.4 MB (228362996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:81b03d74b1b5e3ba328d3c837fdb50abd8524035072f52d675df94d8d92f24af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d6ef62c14d0763cedc2a8976f12513e714bbb30fc5c39ecaaec1b8e4213c45`

```dockerfile
```

-	Layers:
	-	`sha256:77708abedca15714a18685a54d8fb7eb514b2937ff9069400a485b526ac26929`  
		Last Modified: Fri, 30 Jan 2026 23:40:56 GMT  
		Size: 8.5 MB (8510389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a034e140c726d895187f82dbf08feaa4cdea20e3f5d485693adc0c475069d5e`  
		Last Modified: Fri, 30 Jan 2026 23:40:56 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f0f28526328570ff2fc40dfabba2a0770f22c2e302167a9ae412024de5cb84c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.6 MB (384627732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863d2781ff2b60f2ce7f63bad8d498b791e8e0d92c54f76d887935db79389b8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 30 Jan 2026 23:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 30 Jan 2026 23:40:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:07 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:07 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f38b2643584baca69be2b8b70af0343fa74cdb76a88370eb55943870731675`  
		Last Modified: Fri, 30 Jan 2026 23:40:33 GMT  
		Size: 16.1 MB (16071434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cb6bb45ab93038b95733769819a91104c564e2db9e1098d7dd683970a1bba4`  
		Last Modified: Fri, 30 Jan 2026 23:40:37 GMT  
		Size: 226.3 MB (226294066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8cc127d9078efd79ce827e459f9a6c2dd9e233e1fe91fd2afac1880690b26cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42aaefbb13005b327d262a77d30bb068c0795ea9b384e490bf9de4e17b272ac0`

```dockerfile
```

-	Layers:
	-	`sha256:18fb456cf8aa9a403485284305f017894f4259740f2aefa959e9c51dc00606fd`  
		Last Modified: Fri, 30 Jan 2026 23:40:33 GMT  
		Size: 8.7 MB (8705179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bcbefa81b4ae532267353b2496ae5d80662002bf918aa8562feb3f4eaa50cb4`  
		Last Modified: Fri, 30 Jan 2026 23:40:32 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
