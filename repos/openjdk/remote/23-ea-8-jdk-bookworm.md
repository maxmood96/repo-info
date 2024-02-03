## `openjdk:23-ea-8-jdk-bookworm`

```console
$ docker pull openjdk@sha256:4f36fcb5f0cc8a9f4b74479d59c0b8a3b5e1439e38404e8b9fc96c172615d8c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-8-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5eb1f31ae5fd2acb887abb8b14883025edaafd73d61e209f98c211c97e758af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.0 MB (357984061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb08e4e334ad0c6cf374fe4c53eb6ea1a8a9fdcce37c1892d99beab6ce8f74a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a42a6569b9dd1b4d142f86fa90e896819cf50f4808af3b7133d89faacbd0548`  
		Last Modified: Fri, 02 Feb 2024 22:53:46 GMT  
		Size: 16.9 MB (16949162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a128edeb70b27671f868d20375550bfc6316916cae4bfd9a8d705be408e46e3`  
		Last Modified: Fri, 02 Feb 2024 22:53:50 GMT  
		Size: 203.3 MB (203258734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-8-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:baa210ee468eaa08335fcc6dbcb96b98598bbf94b39e80e755a3d699d9c9d46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bdf577e7e17a469e773c3a7a3183c2983013deba00e8edabacf0c850a772e0`

```dockerfile
```

-	Layers:
	-	`sha256:da9df70bf9f68dea8af6570d573ead4682b25374eeee37c4d4ccd92c78cc3ed2`  
		Last Modified: Fri, 02 Feb 2024 22:53:46 GMT  
		Size: 7.1 MB (7116359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da6e032935774afb4476a213f87038a8c91f51549e7ab0a626e9912c1f211a77`  
		Last Modified: Fri, 02 Feb 2024 22:53:45 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json
