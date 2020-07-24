## `openjdk:15-ea-33-oraclelinux7`

```console
$ docker pull openjdk@sha256:a71204a1614e5900d1d3582d8c46b8e486d8a6c225cb760061de760e8ce3b741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-ea-33-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:783e2a001cc92ad834acb3d83f0224e4e64fbaeddd2c36c1eea54a01a433d6e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259961271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c2d3f735fc2b326a7dc1028fcc2b1cf105d151d9885ee048f40fb2deea255e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 17 Jul 2020 02:36:32 GMT
ADD file:0846801b1ef59a7513feb7e2704d8b0c5618da23e28ecff72f64ac14799ee0c1 in / 
# Fri, 17 Jul 2020 02:36:32 GMT
CMD ["/bin/bash"]
# Fri, 17 Jul 2020 02:53:07 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 17 Jul 2020 02:53:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Jul 2020 02:54:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 17 Jul 2020 02:54:21 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 19:14:54 GMT
ENV JAVA_VERSION=15-ea+33
# Fri, 24 Jul 2020 19:15:36 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/33/GPL/openjdk-15-ea+33_linux-aarch64_bin.tar.gz; 			downloadSha256=124fd9ba4611895460ff1547df282cd49b0e9ba2f00c9ead211b59142cc642c4; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/33/GPL/openjdk-15-ea+33_linux-x64_bin.tar.gz; 			downloadSha256=6de169c1de7d37e6c5d5b59a12410a908f22576c07f98d9915a586d91909fc12; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Fri, 24 Jul 2020 19:15:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bce8f778fef067eed3d092243c838d674cb1ef39441d85d0ca84382084a69093`  
		Last Modified: Fri, 17 Jul 2020 02:37:13 GMT  
		Size: 48.0 MB (48014772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778faef342036a08101af5d8806ab4f17eda31d2a4e102e33a115bc619bc019`  
		Last Modified: Fri, 17 Jul 2020 02:58:39 GMT  
		Size: 16.2 MB (16187244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2616704bb3ea954ffa44d36decdfc95c6b7dfb56ec2a28a54094668e5361754d`  
		Last Modified: Fri, 24 Jul 2020 19:20:06 GMT  
		Size: 195.8 MB (195759255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-ea-33-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b87cdc9afb1e2ed74563130f956c44189b26796cd1c059c0a7ccde6c9731bf75
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239936332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e513ee0aaa37cb3cd440e1340a91ecec686d86af9e48e301875ba9bdc30cfe9c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 17 Jul 2020 01:45:21 GMT
ADD file:f07cad218c7e24e1cbce662268da25d9318627f636feebb0f669155354c7f365 in / 
# Fri, 17 Jul 2020 01:45:25 GMT
CMD ["/bin/bash"]
# Fri, 17 Jul 2020 02:03:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 17 Jul 2020 02:03:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Jul 2020 02:06:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 17 Jul 2020 02:06:46 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 19:35:01 GMT
ENV JAVA_VERSION=15-ea+33
# Fri, 24 Jul 2020 19:35:49 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/33/GPL/openjdk-15-ea+33_linux-aarch64_bin.tar.gz; 			downloadSha256=124fd9ba4611895460ff1547df282cd49b0e9ba2f00c9ead211b59142cc642c4; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/33/GPL/openjdk-15-ea+33_linux-x64_bin.tar.gz; 			downloadSha256=6de169c1de7d37e6c5d5b59a12410a908f22576c07f98d9915a586d91909fc12; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Fri, 24 Jul 2020 19:35:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5053e285643065e9638a069d53c6f62fd6bf1d6d4d16001d48a66ee024d7397`  
		Last Modified: Fri, 17 Jul 2020 01:45:56 GMT  
		Size: 48.6 MB (48633508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7d1facfda57a46d98e2882cdeac87e1b92ca135e73948039ab5c8e3c1f5598`  
		Last Modified: Fri, 17 Jul 2020 02:13:50 GMT  
		Size: 16.4 MB (16442484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dee926e341004ce5c5837148b662456c90606f0fd463f5b57bdd85eb7c205b1`  
		Last Modified: Fri, 24 Jul 2020 19:40:48 GMT  
		Size: 174.9 MB (174860340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
