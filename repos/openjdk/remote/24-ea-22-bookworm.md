## `openjdk:24-ea-22-bookworm`

```console
$ docker pull openjdk@sha256:6fd014ef253efce80235ab67ea4fda8cf6dfb4d2abb48ea85f5d6a0017fed36e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-22-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:81608764b85f172c3107d11fc56d9c0f71e07e1b76cb383f62606866479948e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367096902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b75dbc5e6cc97f7e182d1316a3fd5ff9c3611973eb9fd3aacd78ea5750d3e2e`
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
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
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
	-	`sha256:62b71aa9b770b5ff5d01ac3cee501ee1f2fa76e8bbe03e5059508d580576ed51`  
		Last Modified: Mon, 04 Nov 2024 23:07:37 GMT  
		Size: 16.9 MB (16943123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ff5647eb47f26dbc163e9e0318ca839e5b96acf560ae8428356ef4410eb19`  
		Last Modified: Mon, 04 Nov 2024 23:07:40 GMT  
		Size: 212.2 MB (212157675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-22-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4857e17abd7adad3c44266ea4d65852e71257fe7dda53e695802158ece2b924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8445653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ec506a2a85e57e440b17989368c34f79ccaa8737695f63212fc83bcef1a01c`

```dockerfile
```

-	Layers:
	-	`sha256:b4d79bc0f8b4288f527312a7a739dd81b95888ca30a7bee349e8714b2a6011d8`  
		Last Modified: Mon, 04 Nov 2024 23:07:37 GMT  
		Size: 8.4 MB (8427035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a7a55847f6a7de63876fb27c48b38fc52bb63ab5fd092112a83d3fcfedcfac`  
		Last Modified: Mon, 04 Nov 2024 23:07:37 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json
