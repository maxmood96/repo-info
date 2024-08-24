## `openjdk:24-ea-12-jdk-bullseye`

```console
$ docker pull openjdk@sha256:f989ad998e06b8e56de691333ca5821a36940565887ca8d76d227277702fc697
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-12-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:0f04b40f7d71de26abbc8d5c9c6ac137e5275b395514a9e87137be1bd4c1006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351462881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bd5e098141246b7f0a074720c7fc3f80857a16d35e18ed3b2e58a403c5d40e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:29 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Tue, 13 Aug 2024 00:20:30 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:44:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 23 Aug 2024 00:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Aug 2024 00:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_VERSION=24-ea+12
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='9a859e4f3840e3f0890051a26b06413cd18dc8a1b7d68b221f47b38ba2f5add4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='4631ab62c58dbecfc00983df819c9a669b3d4fb681d7f6c3d95af11b7aacf087'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665b6f4bd774e6a4c9738f0532ee622cf3bc07679e5a4449ba05c1f395e4f75`  
		Last Modified: Tue, 13 Aug 2024 00:51:07 GMT  
		Size: 54.6 MB (54588802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1666dfa41ad2af99ef04b15c692c8e4d51d4287ed9cb79f056939f64d667e9b`  
		Last Modified: Fri, 23 Aug 2024 21:11:00 GMT  
		Size: 14.1 MB (14071353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a452db8ff7d5e21f027611061882572516c094a531d0f46a2e7c225706d5b16`  
		Last Modified: Fri, 23 Aug 2024 21:11:03 GMT  
		Size: 212.0 MB (211953798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-12-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a5e89cbfc90c3957e3fb49db62c71aab9952c45c07fea5b7cd74d62ec651237f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8212373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0062e76e1cd31d345a46d2b02d445dfbc3aea08a80c81ff4dd79c45e0964c59`

```dockerfile
```

-	Layers:
	-	`sha256:a06d8c5509afe799187cd1a51bde265feba3580291e6eb5e852935c9af7711f6`  
		Last Modified: Fri, 23 Aug 2024 21:11:00 GMT  
		Size: 8.2 MB (8193910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:261fdc6b76d92e43251a95f29984e59a2888f4a5eb4aa47e3ecc4b2c2867f661`  
		Last Modified: Fri, 23 Aug 2024 21:11:00 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json
