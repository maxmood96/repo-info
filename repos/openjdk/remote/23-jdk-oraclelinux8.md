## `openjdk:23-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:018030754fa68b29611e386db68ad312d88168224b5783622b4920f4176be3d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ec44737a256881abe5e3f5078a58f4d112b253a5e77a04e65089f6e072cec296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278038558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d03249538e2cb2b33e2da6fee9ea78bfe3f3ca370daef59a6ef0a6c38754ff2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Aug 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+35
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='5387c8da8acb4261265c12bb46cea856c248d70bf9d64164019b74ed96545655'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='d5765b057a4eca4913ddd3d661e0ecd9cb182d4ad79359a645e427bdadd574d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce34fc408471253d85d2b44d915ce52e5d485e20cee563dcb6e542ebda1b85c`  
		Last Modified: Mon, 05 Aug 2024 18:58:13 GMT  
		Size: 15.0 MB (15036162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270dee34a38ae85e9dc734184d2e9c8cd333d30e096d1591409361f7f774c248`  
		Last Modified: Mon, 05 Aug 2024 18:58:16 GMT  
		Size: 211.8 MB (211782772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:50ec083cee13983757e52bda61b979888b56efe6e1e570e1b6cad37810d1eb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b440cd47ee9d6bcedaab4c13e2c21191f75d82871388a6d59d3b79e799f8a8`

```dockerfile
```

-	Layers:
	-	`sha256:e06eef80951c5f3705a7bc3ccc55ce8de4fc35efa70c144170fd3ff1509aa5b4`  
		Last Modified: Mon, 05 Aug 2024 18:58:13 GMT  
		Size: 2.3 MB (2287825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcdb51189629ab906713c9bb84c109f0aec37f4c4e258c037b800b0feac9243`  
		Last Modified: Mon, 05 Aug 2024 18:58:13 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b2343c00d86824c4516beb4a333e2f30bbbcb28297ca02f088513f4aa3fbc23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275247655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5f3762c05f2bc7b91b96e3e050506077ed69c8e3e91f84f43f41c48055ddb5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Aug 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+35
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='5387c8da8acb4261265c12bb46cea856c248d70bf9d64164019b74ed96545655'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='d5765b057a4eca4913ddd3d661e0ecd9cb182d4ad79359a645e427bdadd574d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca345db69d5fd49f13cb0fd444dd21dc5576cd6587605dd8acb1793f7ebac2b`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 15.7 MB (15686119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a84396f91f0eeb14da54a9adb3c3dc2a817ae7a902e46666f12df5d31b601d`  
		Last Modified: Mon, 05 Aug 2024 19:12:40 GMT  
		Size: 209.6 MB (209636506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f385cce947573bdb3f66db4b83f83ddbbef3c602f77d5a4c1b4aa230a3a0278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54107326dfa5461027b7105e4c59f34c1f0e653a19c961db5d2f8816692505d`

```dockerfile
```

-	Layers:
	-	`sha256:cfb6c075391fabbf69959b54a3459628463ec8569b7f151435f42a8505ef9ee2`  
		Last Modified: Mon, 05 Aug 2024 19:12:36 GMT  
		Size: 2.3 MB (2287294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381e7a034f14bdf91e7ba47af2c918ad979337faecf04d55a52f57712bb26b7`  
		Last Modified: Mon, 05 Aug 2024 19:12:35 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
