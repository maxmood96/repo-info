## `openjdk:26-ea-32-trixie`

```console
$ docker pull openjdk@sha256:f664042f7780291af17545610bef9ad3345ecb12c7fc5b84f658eec5feb0846b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-32-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:37d35a3383bad8ee6753dce3a3848ead700917f3300868ae3c56de32d292b472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384245976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ede6497c2bce5de60f60cbe52f5e98a196bd6b5847ae3900788850c2a10e1a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:09:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:10:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 26 Jan 2026 22:10:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:10 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:10 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:10:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:10 GMT
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
	-	`sha256:cd9b61504e95f4e780984631244a34ed7a91a4196dccb8eac3dc6c8e7366b5b0`  
		Last Modified: Mon, 26 Jan 2026 22:10:36 GMT  
		Size: 16.1 MB (16071533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62125dab563d15a24bb05118e9c2d6ab108987dc1fe27ddf177b1b008abf6fb`  
		Last Modified: Mon, 26 Jan 2026 22:10:40 GMT  
		Size: 225.9 MB (225912211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-32-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0a7c2bfcaa1408c23963b0a1d2f75863fd236dd8d4c394ecef67e42532041cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39e0ca2e45f640fcc642e1f87dfb01def5499accd0cd64e018f36d73c7effc6`

```dockerfile
```

-	Layers:
	-	`sha256:28c31c87287bdcdcdf6fa66e7bdbe8728e6308c0837938db24c8fe4bc1a7f7b6`  
		Last Modified: Mon, 26 Jan 2026 22:10:36 GMT  
		Size: 8.7 MB (8705808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5098f8cdbdc24a2ab5d0e54f2c36b0824ccad729f2ef0a3f9130424b18539ffb`  
		Last Modified: Mon, 26 Jan 2026 22:10:35 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
