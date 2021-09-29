## `openjdk:18-oraclelinux7`

```console
$ docker pull openjdk@sha256:28fcd609da1d14e759dad9147f80b74283e6c28c6740deb7fb1fbc36ca6388b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:e7d4886c9b12e5b60a6e755cc0a7fe550bb3eeb5ee940ca8df3c9e5a0d136732
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251577829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dfb410de21c6c855bbb805901b02ef678bdab5132b58d4d3f76a4c49912788`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 16:28:42 GMT
ADD file:a9e7957ff3541c254a266620f438cb7ec181b31d50f939d0e687716cefdc7cf8 in / 
# Wed, 29 Sep 2021 16:28:43 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 16:54:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 29 Sep 2021 16:54:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 29 Sep 2021 16:54:15 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 16:54:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 29 Sep 2021 16:54:16 GMT
ENV JAVA_VERSION=18-ea+16
# Wed, 29 Sep 2021 16:54:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/16/GPL/openjdk-18-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='ec604f7aef23624c0acdc0db346a2b226aab47d120538833070f0d5e01d571c1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/16/GPL/openjdk-18-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='623eff3e61bd5f74442fb5699ac3dea167dbe0ade7dd6c1fa9cdd4788e316b96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Sep 2021 16:54:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2294629c97e56d38612a31e50aa9a544bb9ea9a60646d016dcde035fd309dfe8`  
		Last Modified: Wed, 29 Sep 2021 16:30:26 GMT  
		Size: 48.2 MB (48241319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa27d00ff441932dc4be9fc9662577510adff660e4486fa443768e0ca6d260e`  
		Last Modified: Wed, 29 Sep 2021 17:03:16 GMT  
		Size: 15.4 MB (15433173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119745eb87d4fac99bcf1f4ddc5afeb5dd97b15d35dc6b071d2807ed804a6f93`  
		Last Modified: Wed, 29 Sep 2021 17:03:27 GMT  
		Size: 187.9 MB (187903337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fd2f6ccff4767aa4c06291270426f13ab5c28fa54d545094d4958605d7a9c208
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251907746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dc9c78aca0577d8935b4399aceef9c348125fed18353a8658b0016ab60bc4c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 09:28:50 GMT
ADD file:affde62a0aaf80f490cc93e1f691166a15a32c6ef6bc21af35a6659d24c8b6ef in / 
# Wed, 29 Sep 2021 09:28:51 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 10:14:29 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 29 Sep 2021 10:14:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 29 Sep 2021 10:14:30 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 10:14:30 GMT
ENV LANG=en_US.UTF-8
# Wed, 29 Sep 2021 10:14:30 GMT
ENV JAVA_VERSION=18-ea+16
# Wed, 29 Sep 2021 10:14:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/16/GPL/openjdk-18-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='ec604f7aef23624c0acdc0db346a2b226aab47d120538833070f0d5e01d571c1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/16/GPL/openjdk-18-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='623eff3e61bd5f74442fb5699ac3dea167dbe0ade7dd6c1fa9cdd4788e316b96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Sep 2021 10:14:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f5eee715870559160403451bcd7b891478e0df052b7f9456144f3e89e5b994f`  
		Last Modified: Wed, 29 Sep 2021 09:30:28 GMT  
		Size: 48.8 MB (48828923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101207ebea4e1f8fc9adeec0fe8c82c5b0639e2e9c6f0f0bf26e459dc1665d66`  
		Last Modified: Wed, 29 Sep 2021 10:30:47 GMT  
		Size: 16.4 MB (16438786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc84fd83b6cb86ff20243dfff17cd8a7cac13f5c8d23facca6d36a7da74c31`  
		Last Modified: Wed, 29 Sep 2021 10:31:02 GMT  
		Size: 186.6 MB (186640037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
