## `openjdk:26-ea-22-trixie`

```console
$ docker pull openjdk@sha256:4706448e0fa0a3bdbde1be4e2addf74083c170c6b640ecd9530d7c630d5223eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-22-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:185fdb28a0f6570933c04820ae8524940c812652bd12792936c54c597c4ed4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384665833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e00b6b032d0e6a36c6e5cf424f1a127c10319c240d081bf66b48388b53c082a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 11:03:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 11:03:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 11:03:56 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 11:03:56 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 11:03:56 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 11:03:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 11:03:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1435318b309fd089527a353282fc9eb0920a83b2008775463344003fafed2be`  
		Last Modified: Tue, 04 Nov 2025 11:04:34 GMT  
		Size: 16.1 MB (16061561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f0b3b668b7736dd401afd63896377efc1c5d6e9a2986d7c2c5634418e21297`  
		Last Modified: Tue, 04 Nov 2025 13:26:15 GMT  
		Size: 225.9 MB (225926393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d1957a83c50a55ab5c80b9195eeed4a063254689d3986d0ec0485342128296bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8797cd8996b03ea2d08eb508a47e81d84c4302b3c753a646984422f0b4205b`

```dockerfile
```

-	Layers:
	-	`sha256:3b02223811fa33264b571e2cbfcaa9d60d79ecf22df22866e0a37e43feb32d98`  
		Last Modified: Tue, 04 Nov 2025 13:23:25 GMT  
		Size: 8.5 MB (8510528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9759b6c47800801e29050cc8bae359845c4c610006b103fdebb561bb77df4b`  
		Last Modified: Tue, 04 Nov 2025 13:23:26 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-22-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d8cc9be90efe188b3aa9f410635cc112f52d376641f447d390a4720faf129007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 MB (382088400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900f0604c8f950499b5823e3fe347818422b4fc812337245aa3dcb2e6aa2d4d2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:20:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 03:20:01 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 03:20:01 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:20:01 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 03:20:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 03:20:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9dabce176f02cb5c6c71242eba840398fa5705be876e1319c96495fa5be43a`  
		Last Modified: Tue, 04 Nov 2025 03:21:05 GMT  
		Size: 16.1 MB (16070586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506b29b69ab71289f712c17887d0c782c72f54dfd04007375a74e35b8515065`  
		Last Modified: Tue, 04 Nov 2025 10:39:18 GMT  
		Size: 223.8 MB (223765933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:7b29b818db0afe4d4302ba851b13f35404f37848fe3b3b01357d042d6e5fb2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e695d51fd4a46a03ece6cb9156a1629de21f8171a70a341836238f217cd13093`

```dockerfile
```

-	Layers:
	-	`sha256:74c220f43dce9720ff73d34e52296b7d2cdda51cc25b78263ec080b6a98651ea`  
		Last Modified: Tue, 04 Nov 2025 10:23:54 GMT  
		Size: 8.7 MB (8705318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e607b642c2a88ecbffad91e567dc5bbd12acd0f634122b08d5102d6e22f3fcd`  
		Last Modified: Tue, 04 Nov 2025 10:23:55 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
