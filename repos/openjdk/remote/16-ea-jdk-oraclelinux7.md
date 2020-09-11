## `openjdk:16-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:553d949b246697d252f6f86d13d48cc48bfc90d78007e98644d04a3b11810849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:3ae0578256d763373227380450ea5ba69b2e7f4caa1824d0b32e0148fb56b253
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260881630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb071c42725154f75cb06fd23a76ebb50bd1984f41b1f60ed66d20951ed172a`
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
# Fri, 17 Jul 2020 02:53:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 17 Jul 2020 02:53:07 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 22:32:33 GMT
ENV JAVA_VERSION=16-ea+15
# Fri, 11 Sep 2020 22:32:51 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-aarch64_bin.tar.gz; 			downloadSha256=c0fda06a69e492907fe85d1e151e34747e0fce3a2221a70e5dcffd8df048d1db; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-x64_bin.tar.gz; 			downloadSha256=7e6eccd3ac82ce7c007b30a8cde4d849c61612be5353de130690646814f5b9f9; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Sep 2020 22:32:51 GMT
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
	-	`sha256:f4f84bf36947a07c9ae40a2b8718bbe6376d42a4e6a356987de83acd4f2b1436`  
		Last Modified: Fri, 11 Sep 2020 22:37:46 GMT  
		Size: 196.7 MB (196679614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0a28aa54061ae0e326a9069794f70aca501872facac8cf408adf0f08478c00e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240464197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5883b7d1c3664e55d5ae3356d88b0ac2a238acb3c6713080c5924e8a229574`
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
# Fri, 17 Jul 2020 02:03:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 17 Jul 2020 02:03:34 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 23:04:42 GMT
ENV JAVA_VERSION=16-ea+15
# Fri, 11 Sep 2020 23:05:22 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-aarch64_bin.tar.gz; 			downloadSha256=c0fda06a69e492907fe85d1e151e34747e0fce3a2221a70e5dcffd8df048d1db; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-x64_bin.tar.gz; 			downloadSha256=7e6eccd3ac82ce7c007b30a8cde4d849c61612be5353de130690646814f5b9f9; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Sep 2020 23:05:24 GMT
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
	-	`sha256:773a10b0b4497626ade4a8b5d96d41add47bbb0296dc9d3cffbd2b465f636dd2`  
		Last Modified: Fri, 11 Sep 2020 23:09:34 GMT  
		Size: 175.4 MB (175388205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
