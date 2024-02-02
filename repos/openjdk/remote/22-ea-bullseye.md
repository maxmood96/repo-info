## `openjdk:22-ea-bullseye`

```console
$ docker pull openjdk@sha256:9109122e12554032031b5948c1e85e3970168e93362d485df3d82f4b58763443
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:eaee915ebf3bcbbe493df8787a3dee25db6898d7550af6e5f0ee4f13d96e4daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342370501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e70914553718ada8dcbafc98a8cb0eb16a96171f27147985912eea808cdc43`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:48:32 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25b86eb733cf2a10944d7672c8caf1fa66a79321746e004dbb35a1b0007ec4e`  
		Last Modified: Wed, 31 Jan 2024 23:57:32 GMT  
		Size: 14.1 MB (14073002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f6dd5c2de9cb2df8bc26096b0190fe7e0d859fabfb02d69645ac37c423a53`  
		Last Modified: Wed, 31 Jan 2024 23:57:35 GMT  
		Size: 202.9 MB (202874001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:88898196fc55542124bcd2f82ce4e5ea265e205800d3d4b5aeaabb908e11a800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f82e1d94b5dfdbb1d6bbb42820c402f83c7420646af48a5979eb113daf0ec01`

```dockerfile
```

-	Layers:
	-	`sha256:5321574824f7588f6fc276aff920cccf47cff1fdd1551efcffbeb4bd799acf32`  
		Last Modified: Wed, 31 Jan 2024 23:57:31 GMT  
		Size: 7.0 MB (6956084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f671fcdcf3f8a623958a16e5bf51c86bcdbafe03ad8e602d137b4a08781881de`  
		Last Modified: Wed, 31 Jan 2024 23:57:31 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1af242b1e982743cd7009a9a625cf56dcf2a861d9ffeead9ad5029cea36277be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340615552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac7ddcc48130eda7db4cfa534d59073bb78e3791a2a10ad6c572f4cf881ea26`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:48:32 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e361934ac48c39bb74079449b2f9bbddf18b39b92133150271ba85b2d8782bc`  
		Last Modified: Fri, 02 Feb 2024 14:13:35 GMT  
		Size: 15.5 MB (15527406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071de850a379a96d0879e1325aaa237f050cf67a3cf1e907669b0ae6b4d4ae5`  
		Last Modified: Fri, 02 Feb 2024 14:15:18 GMT  
		Size: 200.9 MB (200929323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c1c0bdcba6e6498635c02b1ba6e0232e9a02cdc8393e4814e449f5931e5e0315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5bb18d8c10946e9fd3f90bb8e0068eaf899a2d3a4aa0e16c21065851fa6303`

```dockerfile
```

-	Layers:
	-	`sha256:4a1a682cbe6b6b6c03846d9c18efb0be831524c45c5eb644078c5ac15df2acd9`  
		Last Modified: Fri, 02 Feb 2024 14:15:15 GMT  
		Size: 7.0 MB (7043732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccad3ab6de3b040d68c574bda55f314ef12001498df68a1bca2290a133194eb`  
		Last Modified: Fri, 02 Feb 2024 14:15:14 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
