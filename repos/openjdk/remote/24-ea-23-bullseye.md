## `openjdk:24-ea-23-bullseye`

```console
$ docker pull openjdk@sha256:b4c6fa91aae66f0740f01a0cf1e740f087165d7ee1b913b9323d01ada282601b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-23-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:8e3472145ffeb55f56a710ecf3e1fed6c7f111804aaa99c115878e6270976ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.1 MB (353112580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c3e2ef3f0735202015b1ff7f57f254d9dfc8ea88eef4115f01cbfeafd46c55`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b76a8ffa3e9ea68f7d036f05a099b686200e5b2a734e09ed79775e3485aa637`  
		Last Modified: Sat, 09 Nov 2024 02:08:09 GMT  
		Size: 14.1 MB (14071413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c918ddf4302e27caaa2c20c4da0a7027ebe37f1c39aefc4bc49de82c771457e`  
		Last Modified: Sat, 09 Nov 2024 02:08:14 GMT  
		Size: 213.5 MB (213472955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:03db53fc7db88b5d39f43360d57779e1f3fb711e1ff39c1f9c34adb9344cffed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5158c600ab7dee0c23dadd217c3eaea5d1007d9c42883866b51a736dedcd088d`

```dockerfile
```

-	Layers:
	-	`sha256:23a5711e033f80662e4cd3c0451093690f0ededfdbe8581f4b25db95d1a99240`  
		Last Modified: Sat, 09 Nov 2024 02:08:09 GMT  
		Size: 8.4 MB (8355822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:750caeefed6a884a01c6ddb1bfc17fae7e0e2aa6ad16739b7ddde17fc08558d5`  
		Last Modified: Sat, 09 Nov 2024 02:08:08 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json
