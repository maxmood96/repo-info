## `openjdk:27-ea-6-jdk-bookworm`

```console
$ docker pull openjdk@sha256:e3efb77a523d886539905663438427395c9b02d3079e16b6ec275c51bd4c7600
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-6-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:ded8bcab45a9febc6a37ef3c0dd63f0ac3dada889896502e5c301cfa0c35217b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382190899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf19c101686abd3ceb33ec15b825bed77c9c42f8f962d2379c294cb785744abd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:12:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 26 Jan 2026 22:12:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:12:07 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:12:07 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:12:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:12:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d72bb3beffaeb78d1549bcc9a6777c6fda61d439dcc0430cb65bbb3fe93c728`  
		Last Modified: Mon, 26 Jan 2026 22:12:32 GMT  
		Size: 16.9 MB (16944845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418031c599401d376af4066a8a68484571412b95d53d755bb9b602aee40e8550`  
		Last Modified: Mon, 26 Jan 2026 22:12:36 GMT  
		Size: 228.3 MB (228331732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a7715bc17ac5beb0a28099d1383e50473146dd2fe4078a060068d414d3a4dea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016f3936e3a737faa9d2875a03041c8c8aa8374d9304d9e07d60d5edfc6033ec`

```dockerfile
```

-	Layers:
	-	`sha256:2cd3780d31c71c360590be843d1961c0450255fc29c9ae07d43bf2c588e23c3c`  
		Last Modified: Mon, 26 Jan 2026 22:12:31 GMT  
		Size: 8.7 MB (8668871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf1fe8de2ce114c45f3aa7ef0399347fdca358a2d2c2362c2d827b392105f30`  
		Last Modified: Mon, 26 Jan 2026 22:12:31 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-6-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c84895f67b45d4769aecdf1cbbf98b10cd3738bd89e56b4e001c0e4865244d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.4 MB (380436051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5727df3c56ca25bb4e12dcfeeba96a51c4868c7dcd09bd794b1caba1260ee68f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:11:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 26 Jan 2026 22:11:09 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:11:09 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:11:09 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:11:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:11:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:05 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108765108cfb0be3a922314350c5558a7f5f7342408d950c79037a6df04c9c05`  
		Last Modified: Mon, 26 Jan 2026 22:11:35 GMT  
		Size: 17.7 MB (17728536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294d523ca705e6e5c4934e09066298ca2be9c7fec44ed2c420d0a042aa895966`  
		Last Modified: Mon, 26 Jan 2026 22:11:40 GMT  
		Size: 226.3 MB (226257167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:62e9df5a1ecae4dd9d8daf53556d22accf28284855a427e7a0e45e07a0179121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393d24f6fc1932514d90fa0a2cea8740c3a264b3fc55793423bfb2c167e619ee`

```dockerfile
```

-	Layers:
	-	`sha256:566d4816ab0460042b4416107109862d392fdf913090aed42b7f3961c05f5b5b`  
		Last Modified: Mon, 26 Jan 2026 22:11:35 GMT  
		Size: 8.8 MB (8805716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cf1eed050345d4811094e1fce2226e837de2fffb22fa1c58ac3cf6bc17d533`  
		Last Modified: Mon, 26 Jan 2026 22:11:34 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
