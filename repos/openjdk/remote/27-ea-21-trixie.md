## `openjdk:27-ea-21-trixie`

```console
$ docker pull openjdk@sha256:ad255353ab58cf1f2ca055b99bd222ec65ceec7dd40d9059eb70027c579b22c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-21-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:f0a7bb20256a4c76d9746c409d29e92b4257a5001e645d0c09ae33f947c82f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387539847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0101d0a2a825e7243fe97bd738fd7d925a14b91f165ff4e7cc2cb513d9e858e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:50:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 11 May 2026 23:50:35 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:50:35 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:50:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:50:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7eebb62336d1a2163718afe8fd9fb38532a9fa0a4b501df4f4ece3a0c7b8554`  
		Last Modified: Mon, 11 May 2026 23:51:00 GMT  
		Size: 16.1 MB (16065899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bfb22465dfb2b268f5d7fb94e71a71bd6c9b6684487e7a82d866d2c3c093da`  
		Last Modified: Mon, 11 May 2026 23:51:06 GMT  
		Size: 228.8 MB (228759316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-21-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:76c4c068acbf846b6ea123ceb346fadeee25719c0fb5f000ce5c5f8dd5e71576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13920e07d4730274cad1ab00c57b8a38647959d28a7b94947dd14b0d272c65a`

```dockerfile
```

-	Layers:
	-	`sha256:cf32e9d4d47462faac32d1eff5254c1035e5eab08de916cbd95de51a1e2dd0a0`  
		Last Modified: Mon, 11 May 2026 23:51:00 GMT  
		Size: 8.5 MB (8509920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5beeb1ca4521fbf185fe124c21203982d5d856bcbeb0eedb2f092cf0cdb01b0b`  
		Last Modified: Mon, 11 May 2026 23:50:59 GMT  
		Size: 17.9 KB (17912 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-21-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:579508cd2ccce96b57aec518e5100df8f4e312904c08950d0797ea7db419e7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.1 MB (385082703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7cfa826e893b6ed973d1cdd10c891c32c078c3006b9ad0a081e643c424b884`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:51:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:51:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 11 May 2026 23:51:31 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:51:31 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:51:31 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:51:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:51:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db96c6af88d1174e2cbf3d71056d2985a617c1f44d4ef6d2c2a858c336c58c7`  
		Last Modified: Mon, 11 May 2026 23:51:57 GMT  
		Size: 16.1 MB (16071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8e3a34a50a9c90c07d99589b9052e5cfddaf1c888972c55997b666bf8bf15`  
		Last Modified: Mon, 11 May 2026 23:52:01 GMT  
		Size: 226.7 MB (226726277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-21-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:c2cd8bfaf03a2574fe21cea914547583a13f44ed1c75943b9d87fc9007dc3d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c83a6acfff157274d4372c13f147763839c3c644a4a87cfd229c22f766b564`

```dockerfile
```

-	Layers:
	-	`sha256:af1d824ccb8c196dc614d63d86ededddbda8c65d27155c0fc52a00936bb55d5c`  
		Last Modified: Mon, 11 May 2026 23:52:01 GMT  
		Size: 8.7 MB (8704710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1da46c5e19eb9bd9953f3c9df51a35e22da6264050f47bc91a523b5c17b859e`  
		Last Modified: Mon, 11 May 2026 23:51:56 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
