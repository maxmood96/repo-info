## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:7a4de14687d082c10ce2027a9e47b7e0f238a20364011dee33d10b19d34b716d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c699d474e96486c1f19657476e921a87f42c202cfdf1c6a1661e5d9436387834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278029464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a81bc495fdf46cf2a9e343fea2954795e3b06a761a3e4ffae3b69eceaa7b2f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a684408be1793b9368de30d309361c15dd4150a2ee6403a0b41c7624aca35`  
		Last Modified: Fri, 12 Jul 2024 21:57:47 GMT  
		Size: 15.0 MB (15036186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc4129b37b6d35dbdf3599edd372368d2e52648e9e4aeb53dd9a33eb689b293`  
		Last Modified: Fri, 12 Jul 2024 21:57:51 GMT  
		Size: 211.8 MB (211773654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:bccf20efc522beb321a000c623d951b68d41f54786ebf7521e5ef9fd7bf480ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cfe335a001d87fc79c3b7d9eb46e984a534227c2dfb846ad050931639980cf`

```dockerfile
```

-	Layers:
	-	`sha256:8910856d0fb5bcacd4cd4df7e1d2907969f338beca7dbcbfecf47f528387b47b`  
		Last Modified: Fri, 12 Jul 2024 21:57:46 GMT  
		Size: 2.3 MB (2267577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8296fe3ad014167b6150af351b0673a8fc3fd762de477af19b09ee28e848e300`  
		Last Modified: Fri, 12 Jul 2024 21:57:46 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2aed254ac045e74f1c0ffb44ff49ff6bd9fa36e8c60a8c786bd54435b9c0542c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275252631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbab39cc9280fcae66db1b2c4782edcca856b30da06601c281b4299c61c65e4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53325ebdf5962703e657719964570a5baf1824ea843ea45441c78f115b80fb18`  
		Last Modified: Wed, 03 Jul 2024 23:56:52 GMT  
		Size: 15.7 MB (15686023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bf3d61820d6aaf8a3d3989748c0d6e8164ceabd83f86791e83a5cb6321b97f`  
		Last Modified: Fri, 12 Jul 2024 22:11:22 GMT  
		Size: 209.6 MB (209641578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9a1e45b745d8c953990feda5fb86308fed2284e7f1665c674e68af4e22c85157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904af5e33f693d83d9271d8a0e7df8d3f0cafc8250f4a36c1e30656911b65f38`

```dockerfile
```

-	Layers:
	-	`sha256:57c117cbee33c2b8410d1546a85aa7b20ee27d503e647341741782293935ea81`  
		Last Modified: Fri, 12 Jul 2024 22:11:18 GMT  
		Size: 2.3 MB (2267046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdc55ffed4b7a25aed72d8d0bcd1bf05bb149dab1d3ab4d5d86a3f8f63f567cd`  
		Last Modified: Fri, 12 Jul 2024 22:11:17 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
