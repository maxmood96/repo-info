## `openjdk:25-rc-jdk-bookworm`

```console
$ docker pull openjdk@sha256:8f97e0d6d0450b0ad399863b597bc0ea67f9c262c66d35283dc89100bf8cae5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:33c678310235ec011488ff68c4f8eb346cbd0d03f79f46e7968999c06a6401d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 MB (377047824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8242346385b5a893c90b11ae919bd9d921d88697c151283babcb47f5244883`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
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
	-	`sha256:7cdf2fa82db23af8dfef4f51dddf118a5ff7ec9f60cdf8d465f97b4b63855ed0`  
		Last Modified: Mon, 18 Aug 2025 18:16:38 GMT  
		Size: 16.9 MB (16943424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928e5f3296d409eaf4296071da3124dfac88303ea7dcdb6ba5f39757c5aae477`  
		Last Modified: Mon, 18 Aug 2025 21:25:35 GMT  
		Size: 223.2 MB (223188998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:dc89407dd6de6c468190d856d1b7cf41fd4b6d3c6ea49154c6ce95acce33d8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8682562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc0120b0637f5ac2ce6f20c053e2e3eca8b3f53429e8592190944fbc9c65531`

```dockerfile
```

-	Layers:
	-	`sha256:45d48992079c1ea7d108cb784346e610b04926da3f8240955a53c3f67c0457d4`  
		Last Modified: Mon, 18 Aug 2025 21:23:27 GMT  
		Size: 8.7 MB (8664532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23275006c1efffc343a4c9b1c3f14013bf37834524fd05ef5acecb9f93e5f9c6`  
		Last Modified: Mon, 18 Aug 2025 21:23:28 GMT  
		Size: 18.0 KB (18030 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cee277807f03ab1cd60ca44a6767a92fc434d063e877842ccd9e4851c2f8a3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.0 MB (374980946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10ff39269783e4238310313ebd92519d5a14cda51a5d3be7441f3d57dee391a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224c8c5b8dff524256200adc53415a0d5db5444327a968400e64baa4d5ddfa61`  
		Last Modified: Mon, 18 Aug 2025 22:24:53 GMT  
		Size: 17.7 MB (17727544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bd231de1cfd17f62cf8f506da154f753d662a897b0e472ea525b0fca1e8849`  
		Last Modified: Mon, 18 Aug 2025 22:37:07 GMT  
		Size: 221.0 MB (220974102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:79043a48e6ae87778dcf084575b075870ed5beb3fbf130ed864baf6917d2151b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8819526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9749f7e22586a2d8db321a338fc883cef956157d3a9e20e2017eca5695c078`

```dockerfile
```

-	Layers:
	-	`sha256:3207c5b79ce51f24815e39edaa092ea91ad2c2938716062940fd0a77e2d5ebf7`  
		Last Modified: Tue, 19 Aug 2025 00:23:32 GMT  
		Size: 8.8 MB (8801377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75c21a6c5fd2dd51c03c4ad731168b67c70eec3a76dbf9308da903e11622c37`  
		Last Modified: Tue, 19 Aug 2025 00:23:33 GMT  
		Size: 18.1 KB (18149 bytes)  
		MIME: application/vnd.in-toto+json
