## `openjdk:24-ea-23-bookworm`

```console
$ docker pull openjdk@sha256:1d2019b3fdb98d800d6687d3eb271304d131c804e0f1a0d95d0b4d9631756306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-23-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:4d712987fc5b064ceb3563775568bcc3e6214de2a66c705e316ad9b5b74a12d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368420389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83eb37e2f6993223f6647f4dbd669d09adfa7e179be68969ad3a019f136a668`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 07 Nov 2024 19:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='4a83df6c5ba87f963cb8f7830f1ddef7dbe387b6884749411cdd4db6f3be6ee4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='76fba0034d8bd3edd8983162ebe459dfcdeb8d19e0202eb42803716fedf61a32'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86d04726c2640a955c91428adf24137c35a77a067bf428cbb0cf47c9d2f0c2`  
		Last Modified: Sat, 09 Nov 2024 02:06:54 GMT  
		Size: 16.9 MB (16942971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a819a6185072d0e5245740fee4054967b69ede16133795177644f7768c8d421`  
		Last Modified: Sat, 09 Nov 2024 02:06:58 GMT  
		Size: 213.5 MB (213481314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-23-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:83ed3f1608a5a62e12bee8ce0d00a244801eba4edce0e53e82b29c6f9593a1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8445653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c835f0e001ae045b9ff5f716a17d0cdb6eee9a24beadba879ee88916f7b7cf3`

```dockerfile
```

-	Layers:
	-	`sha256:b1d0cab9e5b5f5dc085720fca24754e9df28d9a04142949c1b2fc52daeb276ed`  
		Last Modified: Sat, 09 Nov 2024 02:06:53 GMT  
		Size: 8.4 MB (8427035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c7c43dc7f8004dab4a0e600b7daf683541d5f6da7225f29134019bde3cfb42`  
		Last Modified: Sat, 09 Nov 2024 02:06:53 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json
