## `openjdk:25-ea-20-jdk-bullseye`

```console
$ docker pull openjdk@sha256:c9ed0c63d946dbe4e1a56a22cf8824a6b0deb72004f339d911fd0c6c9c658315
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-20-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:51d27493dfd3e53746fe032200e252922668fb0a1113159cbb8df8de31ec6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350845264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eb622883f1351ba6a64f57f3cdf3f1ef1e3ed84d188b53b9a22a579933e673`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e678da5788f5055963a1639748b2eb392d681b04e5baee844b89436893b741b`  
		Last Modified: Mon, 28 Apr 2025 23:12:14 GMT  
		Size: 14.1 MB (14071378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db91dfdab88a938d404578c1084f3dc4bc38518aaa7acafdad187aca6b94a0c1`  
		Last Modified: Mon, 28 Apr 2025 23:12:17 GMT  
		Size: 212.5 MB (212506596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-20-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3c6b812b198b01dc27c1a3994edb8c97600d38c87125c0ed3c6ff0dcea209e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbabb29c8cae326badc764ae9c583bd62e0470c0441d42158db9f54ef7c3bfb6`

```dockerfile
```

-	Layers:
	-	`sha256:0a9a9cce30ab260ce6b4f4c487a466012839c9d906f1ed1b456354eba9b0c6ad`  
		Last Modified: Mon, 28 Apr 2025 23:12:13 GMT  
		Size: 8.4 MB (8366190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a15cafa501bbd9460f0b4a7ec173f2edf7571e4b3e1eb6ec4060222784b297`  
		Last Modified: Mon, 28 Apr 2025 23:12:13 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-20-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c5f41b279ef61ed2b37faec538c5132effe37d2ac78fe9b115daa26682e4304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.7 MB (348705455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efa33f8512d1dc4b91e5c0bbb52cb8f1141f4d9d2dd4679e81db90b9b5de9e5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e083c302b4f5ef95e7f103ab22b947c3e67397db7ff914707f08c59f2ec6b5`  
		Last Modified: Wed, 30 Apr 2025 03:54:13 GMT  
		Size: 15.5 MB (15526614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11649d5cb383e9325b96d76e618a2195f54ff1c60da9ea68e5ac3e8dbd17853f`  
		Last Modified: Wed, 30 Apr 2025 03:54:17 GMT  
		Size: 210.3 MB (210333753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-20-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0a39bdb4e240b55c1aaef99fef4f5de269340ff5a2193669c1c13b3ce5103184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8485913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238b285cde58b15a72aec0b037fdd378404c97ad3aa1bf74f5befd4347f2322b`

```dockerfile
```

-	Layers:
	-	`sha256:cf9b3223f98024a81f0e18735bae65dd30e74c13c56cdb883bd615ea557223da`  
		Last Modified: Wed, 30 Apr 2025 03:54:13 GMT  
		Size: 8.5 MB (8467152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f76511a779763d908c52afca8f9a6ec0c201b79cb0633e9046907bdb7cb307`  
		Last Modified: Wed, 30 Apr 2025 03:54:12 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
