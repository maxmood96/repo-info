## `openjdk:25-ea-21-bullseye`

```console
$ docker pull openjdk@sha256:b842ef01018b58b9458645566bfd8f30cc7a6e008b6fac25a144593a3968046f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:25-ea-21-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:355c39d34018304423171b4b879425392a08081aa247fdd18ac02c1190f587fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351735040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57dc8e0282d9959379fc0e741da7fdd69e523a8960df709b618afd133a6f5df2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 03 May 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 May 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_VERSION=25-ea+21
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='9215df470d2d44c8ea731dcde9e170b6951e29f6e96e90625be983f0f9cfd1ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='23b6cbdac4dedcb1e7d290e7f5e9da01be8c4dcc35b4d296054aae3588d4465a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 03 May 2025 00:48:11 GMT
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
	-	`sha256:9063283694ef91bfc90202649c7ecc42c8660ee7a1a967e924329b370631a3d7`  
		Last Modified: Mon, 05 May 2025 17:30:11 GMT  
		Size: 14.1 MB (14071504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1363f9c564f73f2046bbd9e5d6a046a80f5c473a342b93b3ec20fc4f03ba`  
		Last Modified: Mon, 05 May 2025 17:30:15 GMT  
		Size: 213.4 MB (213396246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-21-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ecf7f3d9700bffe79adbec490cf7e90388f0b84060940bb3c8119708cdb6dd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941d5c674844e602ddff324a93f5239228c5e8d35f2db30b1825130102c4dda9`

```dockerfile
```

-	Layers:
	-	`sha256:1582599e414800d5839c81eb2f846147280136ff736fa9a6b9bc9bcf16441796`  
		Last Modified: Mon, 05 May 2025 17:30:11 GMT  
		Size: 8.4 MB (8366190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84a5ef678044429a2ef749804a4c146c4954a24064926e403d7ab84dd17dfdd6`  
		Last Modified: Mon, 05 May 2025 17:30:11 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json
