## `openjdk:18-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:06d003927e9873bb6ed7eec66f5479663e69abbcc1b2fee4c0ec128deb5ce101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:feefadca3ffeaa5da10006b7a16a220c34d5a45abfba9f9b6d031d276f8ff6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251229079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889581983ec82e9b39560f2f40daa61c196ea2386d8453732092a4588f14710a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 16:51:20 GMT
ADD file:46efe0cb70a1c4f574c3b3e1fb9b9733930d246bb8077c4ec2160a840697e6c8 in / 
# Thu, 17 Jun 2021 16:51:21 GMT
CMD ["/bin/bash"]
# Thu, 17 Jun 2021 17:08:18 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 17 Jun 2021 17:08:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 17 Jun 2021 17:08:19 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jun 2021 17:08:19 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Jul 2021 21:20:50 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:21:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='03f895bdf47691e44e9b269eda74f407715e97385b0cfb60304bcfda29f589a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='bc3dec6f82541afbd83e9b5ba6ae70541206accd7d815dd171fd36c93a90fe3d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 21:21:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7627bfb99533146fcb8374f557bc24c36505fb2ee8578ec6072a821200247bbb`  
		Last Modified: Thu, 17 Jun 2021 16:52:21 GMT  
		Size: 48.3 MB (48260810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb70fb8946cabfaff2f43cee5915a69ad662b0294e9c91d8f545898e92ed32fd`  
		Last Modified: Thu, 17 Jun 2021 17:14:39 GMT  
		Size: 15.4 MB (15426613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c6d4b42c597f370b04e0d4b829ac62198be549e4a52fe163bbd92c43ea7c97`  
		Last Modified: Fri, 23 Jul 2021 21:27:18 GMT  
		Size: 187.5 MB (187541656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dcc8c1bac728b69831fc22ada6a0683a2ddb36e0cad1e244e0183150c7f0393b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251550666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38574e473967496573354b7dea3a002b1fea3f595c2ccd23b9d32335d645022b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 16:51:08 GMT
ADD file:256f7e1c19fbbacd7c7650e1e9991f3617703ba349f259624d78e4393e945665 in / 
# Thu, 17 Jun 2021 16:51:08 GMT
CMD ["/bin/bash"]
# Thu, 17 Jun 2021 17:08:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 17 Jun 2021 17:08:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 17 Jun 2021 17:08:43 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jun 2021 17:08:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Jul 2021 21:41:03 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:41:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='03f895bdf47691e44e9b269eda74f407715e97385b0cfb60304bcfda29f589a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='bc3dec6f82541afbd83e9b5ba6ae70541206accd7d815dd171fd36c93a90fe3d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 21:41:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a3d615f016c21e1c5fef521352cdd990a61abfd09a26d7124c61e33b2cab56a`  
		Last Modified: Thu, 17 Jun 2021 16:52:10 GMT  
		Size: 48.9 MB (48858581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4a33d75d2c35cdf1c0dc42b99124399c0375b12141be4bddb4b819732453cb`  
		Last Modified: Thu, 17 Jun 2021 17:23:33 GMT  
		Size: 16.4 MB (16419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf37ed0d6095f5ebf55ec80e4fdb63fe75c1ae6a4bccd751f5b250d11e90af1`  
		Last Modified: Fri, 23 Jul 2021 21:53:04 GMT  
		Size: 186.3 MB (186272379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
