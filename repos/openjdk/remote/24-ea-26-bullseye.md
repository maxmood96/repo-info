## `openjdk:24-ea-26-bullseye`

```console
$ docker pull openjdk@sha256:57b443ec2ae5e4bb964941437e621d5149c2f30b5810ddf87029aa544dfb80f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-26-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:35ecca92ffbbc50d4da5dca246cf9c5e010373619208820c5d1df4fb865a974b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350859579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7356a5d11d378c52eddd725a66ef566e4fad2d95dea6dd60247e96c27a85f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Mon, 02 Dec 2024 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 19:48:14 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 19:48:14 GMT
ENV JAVA_VERSION=24-ea+26
# Mon, 02 Dec 2024 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='5a912c97361c098aaee25aa395745f77456ec2af1541c1aaa707b20f20e50fb8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='fd075f47c3ef0e3e6270244864a33309becf3f2fbdff615d20a86ea15779caf1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b6c45f66d6f4288ec8324ba147ce6f144b44e4be3b962958835962c5b790d9`  
		Last Modified: Tue, 03 Dec 2024 16:32:22 GMT  
		Size: 14.1 MB (14071356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79577177b63ccdd478406c54a1808bb9e46ec7839715b042e1543666f5b98878`  
		Last Modified: Tue, 03 Dec 2024 16:32:29 GMT  
		Size: 212.7 MB (212736717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-26-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3e0c647126311c9808e8f9dee5f1db6fd8ce55002f815efe62e1a0bde3e07cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8389534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c72a87ff8eee7be4ef9108cd083e8962bb9e36f9919fc3f77670be4441af400`

```dockerfile
```

-	Layers:
	-	`sha256:dcea0d79b6366ea0021b5779be02fb89e062d094fd97e8f1fceaf02aebf12417`  
		Last Modified: Tue, 03 Dec 2024 16:32:22 GMT  
		Size: 8.4 MB (8370918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad96e59c93996e3ad21392c25cd51b97650e8d5f1a3a21086a50f9b29fd3ed7d`  
		Last Modified: Tue, 03 Dec 2024 16:32:21 GMT  
		Size: 18.6 KB (18616 bytes)  
		MIME: application/vnd.in-toto+json
