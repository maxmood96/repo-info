## `openjdk:26-ea-13-jdk-bookworm`

```console
$ docker pull openjdk@sha256:9dbedff7830871e1fab54a6be3ca95b2bf982e0c7906cb1ff728b4c92c67af67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:26-ea-13-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:fe5ba5f3cadb68eaceb04afb06691fc350cbc162bdcb72b518e819bcd6e3065c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 MB (377149718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383f2ab651f59999f2ee0f8c211ef065ffbd0acc9096b4fa3d6e65e422bde07d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c2971fa4e003a0c22ccfedeb5f316c9279a8f638b97ded7c1ab0142fae5ade`  
		Last Modified: Tue, 02 Sep 2025 17:24:06 GMT  
		Size: 16.9 MB (16943523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6fc3727f97c1abefb65182d7507be2f9e721bed5b04547565f8fba8dfb648`  
		Last Modified: Tue, 02 Sep 2025 18:29:24 GMT  
		Size: 223.3 MB (223290793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-13-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7194d6022c9e61714cbbdc3b4785c5e70d391a5d45571829469241976a66726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8683184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bc4420916ed7d1e69af51c415e868a47895415dc4c42c609a6023e6e8898ab`

```dockerfile
```

-	Layers:
	-	`sha256:07c8c505ca3cdc791b26b58862aebba1424b55a831cb4a08b869d3283f5cf8e1`  
		Last Modified: Tue, 02 Sep 2025 18:24:03 GMT  
		Size: 8.7 MB (8664566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec33da98297afecff19fc9c2781c90d6b0769a547af887ace5ff3c821f6a695`  
		Last Modified: Tue, 02 Sep 2025 18:24:04 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json
