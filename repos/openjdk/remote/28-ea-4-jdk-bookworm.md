## `openjdk:28-ea-4-jdk-bookworm`

```console
$ docker pull openjdk@sha256:22d62d87cf6476aa5da8a44fc7e3a380d2dded98dd82c1176ca9c62e3cd3b726
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-4-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:cba184dc08e747538d5be465554ba0f1e3c71ea3023e62ab731714a5ec856d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 MB (381421266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f2ebe0330fee3573aa8c9db213e76314c56ae053ce017cf13d638bbcd35cf1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:49:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Fri, 26 Jun 2026 17:49:59 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:49:59 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:49:59 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:49:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:49:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd7bf6f6036613e20f62549df75ed694b99118002358bea5a81baf3929d1ff`  
		Last Modified: Wed, 24 Jun 2026 01:41:33 GMT  
		Size: 24.0 MB (24044046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791c68bc2063683c3d15907b8ed1b777cf14ca153c6f8e5b12db0868dfa7e38a`  
		Last Modified: Wed, 24 Jun 2026 02:28:33 GMT  
		Size: 64.4 MB (64404017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de04115d5ef9e64548844f860b3eb67175e492be9292a7068d028d0d834c862`  
		Last Modified: Fri, 26 Jun 2026 17:50:24 GMT  
		Size: 16.9 MB (16946496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9236de99735479ee06e8c8c9b17f1ae32eec293dd0a27f4edab3c07fa2d8c3ca`  
		Last Modified: Fri, 26 Jun 2026 17:50:28 GMT  
		Size: 227.5 MB (227524497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-4-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:18b2a7121abd420774da6c82b437f39c5212082f044dcc4d9801aa774d724885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33423b3e44a916a1103682b36b094e23ea2c2b581a2b1536b8cc47e9a73da5b`

```dockerfile
```

-	Layers:
	-	`sha256:4e3c4f1ad60310a34d2017412151f7e9a68cfac4cdff60f6842b2d4f3a05fbe6`  
		Last Modified: Fri, 26 Jun 2026 17:50:24 GMT  
		Size: 8.7 MB (8666366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca8d685ba969f1f9b8aaea72405df77a7783d98297952a77de7001c1dd47966`  
		Last Modified: Fri, 26 Jun 2026 17:50:23 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-4-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b029ce5ac1cae84aa9cd9d1894cb8bbc02e046bd09491636597d25c023ee5094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 MB (379793209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e929ade40a0fd2edb133eaa3559b38eeabef5ff48ee06f56f0e133c23fe49`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:54:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Fri, 26 Jun 2026 17:54:54 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:54 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:54 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:54:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebca214f1a4b66acfdb0bd20aa3ee139d1747885ef4b0f3d07aa2a68459230`  
		Last Modified: Wed, 24 Jun 2026 01:44:48 GMT  
		Size: 23.6 MB (23613316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bb0e918720911be6cb7a1a5ba9ad0e1a308fcbf24961a23aba0cd220df6cf`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 64.5 MB (64487706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6506f301f81883712adb5b873e345c4099051abbc618e645da439c4b2b8cf`  
		Last Modified: Fri, 26 Jun 2026 17:55:20 GMT  
		Size: 17.7 MB (17730317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e68afa4ef80e6ba25639b1d32f5ba2a0e7135d133ef559652de66dd0700da0`  
		Last Modified: Fri, 26 Jun 2026 17:55:24 GMT  
		Size: 225.6 MB (225572669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-4-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f5c082eea1947dbe262fa22714b5c14d3b84c62e041388cffd760c05bcf9ecf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a64b4aaaec6880c6d3640e495600dadd79c8c1b57159ba80faaf1973ed2286`

```dockerfile
```

-	Layers:
	-	`sha256:c8f59b13c7df329a53095d0f82fa0a9aa420aaaaf78a9bdcd27847401c1bb24e`  
		Last Modified: Fri, 26 Jun 2026 17:55:20 GMT  
		Size: 8.8 MB (8803211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d03adce7612738bfa5d8b61bace9c4febf368882eccde41fc31a10a414bb91b`  
		Last Modified: Fri, 26 Jun 2026 17:55:19 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
