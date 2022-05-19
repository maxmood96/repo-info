## `openjdk:oraclelinux7`

```console
$ docker pull openjdk@sha256:3e42408a253339d512a1fd88c84bee2498b644c72866b1a4c9a802daeb799fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:c61aab6815aa3bd747564cfe752e9b844103a95fe933aabd7d703f6cee7ddad2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250522761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af3d351403d218608d70c9ebaa42f145868f54cbedc6e2c747ea33acab2b638`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Tue, 29 Mar 2022 23:06:58 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 29 Mar 2022 23:09:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 29 Mar 2022 23:09:26 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:09:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Mar 2022 23:09:26 GMT
ENV JAVA_VERSION=17.0.2
# Tue, 29 Mar 2022 23:09:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:09:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80558a30268385e2f78e93d6dcd977e92f7c76354c6ca130dd3ac4cb4b90f212`  
		Last Modified: Tue, 29 Mar 2022 23:18:51 GMT  
		Size: 14.2 MB (14239096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79afd9053a5a3b76ddb647b0ac1c703e05377b1df84c7a28994207cc611f1aa2`  
		Last Modified: Tue, 29 Mar 2022 23:23:45 GMT  
		Size: 187.5 MB (187526182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:591430099e0658f83e37f6bfcd0b3a088fc0d3bf3ac06b052e265178c8bc63e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252255055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717d3a66bda1fbd11d1ce3f712a5987bec1074278cbdf2a98d1936257c341a17`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 May 2022 22:09:29 GMT
ADD file:b866e521d7e920b2210ec5ba4013715f28d1ad0636a38a13cec969d5b3586d44 in / 
# Thu, 12 May 2022 22:09:30 GMT
CMD ["/bin/bash"]
# Fri, 13 May 2022 00:26:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 13 May 2022 00:27:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 13 May 2022 00:27:15 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 May 2022 00:27:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 May 2022 00:27:17 GMT
ENV JAVA_VERSION=18.0.1.1
# Fri, 13 May 2022 00:27:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 May 2022 00:27:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa569c775ec815d1a2d6e7b4f6e989b8afe4f0749c119d04101e4cb016365983`  
		Last Modified: Thu, 12 May 2022 22:10:25 GMT  
		Size: 49.3 MB (49340765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a850683079b99a0cee3fbeb957ff22bf46a963d7306f33b059cba19183ee75a`  
		Last Modified: Fri, 13 May 2022 00:37:40 GMT  
		Size: 15.3 MB (15269457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb2abd35e4d557c2be35953975054fec6fd8cab25ea35f67bec4401d6c403c0`  
		Last Modified: Fri, 13 May 2022 00:39:05 GMT  
		Size: 187.6 MB (187644833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
