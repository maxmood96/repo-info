## `openjdk:25-jdk-bullseye`

```console
$ docker pull openjdk@sha256:833b99170abe72e4a5ec827324c3575aebbd64e910c1b41c22380cc5ce51d322
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:dc6b6ae2a4fc6b4c68849eedf85a87fa9936b71d5dac8f3c6bbb1d998b792f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (350038183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d7bf4356346a6c00eb43a6b07091a70afbaaffa49b0dd16cdb0b4e67a46831`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322d21cc1b9c3e86a0528fd885e7483a3b2497c1448256bf87a4493be665ab0`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 54.8 MB (54752320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea20f402889bf4bdc874df3eb08d3be674755cea0d9a6e24ef16c91e2b103b87`  
		Last Modified: Fri, 21 Mar 2025 17:13:01 GMT  
		Size: 14.1 MB (14071422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24338850141060f6b7fea6fdbfa69aa5a44d2e2591928f933a9e9f03c6fa423`  
		Last Modified: Fri, 21 Mar 2025 17:13:04 GMT  
		Size: 211.9 MB (211914811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:34aec676a6ca9974dbe1ee6c45a57bc94e3c6a11109304d64644fbf97ddb2904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8382792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611339b37f95bc5f484f1033275d9920364c2b10f999f55e47252d60562fd3f4`

```dockerfile
```

-	Layers:
	-	`sha256:091ac6869f28e153bebc7c8ccb35bd60c8af1bfbfa79fd9cbe30a48dd76f4068`  
		Last Modified: Fri, 21 Mar 2025 17:13:01 GMT  
		Size: 8.4 MB (8364174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f6d769ad875b60d9f9a3f2a38b728338f5147d49457b852f70c6f46199c29e0`  
		Last Modified: Fri, 21 Mar 2025 17:13:01 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6683e93d138719870061aa59187dd2cda8f23e74bc0db28b0deda38758424cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (348048693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c980dd23321f5c4a326176b2f1e48b1e96d12d231cf5fc984779c2859ba1252`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b658ea4b94c216c095b98c1eaf64a94c74a484b39c3f0e7317d2f74172b5b4`  
		Last Modified: Fri, 21 Mar 2025 17:27:33 GMT  
		Size: 15.5 MB (15526350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecf21672121302dace2a21d347d5593330051c2325cd9a5a56b144b97d80924`  
		Last Modified: Fri, 21 Mar 2025 17:27:38 GMT  
		Size: 209.9 MB (209874516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6a3c70ed3372ff887daa0890e53fcab218465f68b79a12a43f86a2b6f15858c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8483897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6546df58dc84494798573198bda646286bb79b4a056152a53446f7d173d2a3a`

```dockerfile
```

-	Layers:
	-	`sha256:cac713d74527aeb0597425320b76c4746c5e63a9d1159e92088046e6d6ee5fc3`  
		Last Modified: Fri, 21 Mar 2025 17:27:33 GMT  
		Size: 8.5 MB (8465136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12f980ffd0edaec8ac62bdd4806c8bff509ff7ba0be68b874de284a83a9c7b1a`  
		Last Modified: Fri, 21 Mar 2025 17:27:33 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
