## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:102345740ecc06984295075dc5dbf9fc6d27b57d2a2317050250227286a71c77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:874c8c3a325438b38716683c2e2b2aaf86c9a31dbd641cb8d0f51ea187e78fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278442161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb18db70d7a5b9bd849d9632dc366216a15c2be82a31256d8d289116a3a3682`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e80e886fc0695bdbd16b2a62c3899203a2f2b913947261d3ff7de907426b81`  
		Last Modified: Mon, 29 Jul 2024 16:56:51 GMT  
		Size: 15.0 MB (15036245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ca93a22ecfd36ccef6bc551d13e6cb1b15bacff59bc492a8c42d2b316c024f`  
		Last Modified: Mon, 29 Jul 2024 16:56:54 GMT  
		Size: 212.2 MB (212186292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ea4f15276c33b6fc663ca74da4889592e7cd5529f14e859cdf3bbf985670825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c58e849975d5a16bc7682552b4349e4ed145a34a4b7bcb21c80ffc114f0fec`

```dockerfile
```

-	Layers:
	-	`sha256:311acd226e7281ab7d4e8181ec37a4122b9c07a87ad0437437f265c1964c6958`  
		Last Modified: Mon, 29 Jul 2024 16:56:51 GMT  
		Size: 2.3 MB (2287817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76dc816afded124d25f7ab24f6c2ad69a4ad5d46bf7bab3367941cd8eec4576`  
		Last Modified: Mon, 29 Jul 2024 16:56:51 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c9974164348a49662e32d47af00f29954eb5684be2ffca1fc6cfaade9bec6d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275672474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3312ef02929a836e140af10cdaf59e969255065c80f962a9da00098b7260d4d3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
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
	-	`sha256:7f9438a872169f2b29e96ff157de619e45c4c52cdaf23830889a100783798bbe`  
		Last Modified: Mon, 29 Jul 2024 16:58:00 GMT  
		Size: 210.1 MB (210061325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5afde9a106f705e4f718e8c76a3b8ec325330614864376bc3bccc79535054aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17ad95baca5dfbca4ea4daddee0a95676cf9becb2ca9077c68f9d811dad0eef`

```dockerfile
```

-	Layers:
	-	`sha256:323070749bbe1d1f8aaf789d67b5096dd505bd740a743299bd4247159b832ed7`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 2.3 MB (2287286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1ceb5f864825f1a397c35163a6b05e11c00e2a6370c6733dad276aba3f7435d`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json
