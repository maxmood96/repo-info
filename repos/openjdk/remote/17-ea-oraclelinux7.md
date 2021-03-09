## `openjdk:17-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:0f022421227d31d2101039be9fd4dca16839f1c4bf56c83f867d7ff3f6a216e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:dbff0aeb38fc665cf8728d5462569c286c8d57bbc7d03250854589dba00b8a5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249408698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f82b4d7150069487d4fff2230ba2d7f13f51dff2d10d18b80144ca8d19b9f61`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Mar 2021 20:36:55 GMT
ADD file:361f165903526126476b03dd2afac1fff0b334906bb56d024e5aee87b948b0cf in / 
# Tue, 09 Mar 2021 20:36:56 GMT
CMD ["/bin/bash"]
# Tue, 09 Mar 2021 20:56:14 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 09 Mar 2021 20:56:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 09 Mar 2021 20:56:14 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 20:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Mar 2021 20:56:15 GMT
ENV JAVA_VERSION=17-ea+12
# Tue, 09 Mar 2021 20:56:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='e281f7d1fd2aaa858b02d5be451c51a9ed836c78d002cb82b114e6c36041eebf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ae713390655d0cfd8302cb2c840553404a3e366162ba5b9a2410ea7b6f1c27'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 09 Mar 2021 20:56:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a61503a3b32ea964eb926d54dcfe6cd7e21f4e0cca1b1373df21cf904388c445`  
		Last Modified: Fri, 12 Feb 2021 00:54:42 GMT  
		Size: 48.3 MB (48263629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bec9c0e7fad6eb1470aa0268ede53633bb156c1b1700c2347ea7c1b36ddfaba`  
		Last Modified: Tue, 09 Mar 2021 21:09:25 GMT  
		Size: 15.4 MB (15439846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e278b8f38b279b5666457e146ef57a569d5ca842a7fdcc8ffb986d26beec469`  
		Last Modified: Tue, 09 Mar 2021 21:09:38 GMT  
		Size: 185.7 MB (185705223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bdbc5e8708080510ceb409fd22be4294f5f5d67a9c75b2bfc16e64614dd8ddaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247052805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a670adfa8aa512739e87c364c062007a3e06ffd592e1eaaceb24c1934e764918`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Feb 2021 01:00:40 GMT
ADD file:25b64ec41b7ca742c671c416e08a7bee3224e4052650624ef31b5583b1c412df in / 
# Fri, 12 Feb 2021 01:00:41 GMT
CMD ["/bin/bash"]
# Fri, 12 Feb 2021 01:19:33 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 12 Feb 2021 01:19:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 12 Feb 2021 01:19:35 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Feb 2021 01:19:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Mar 2021 01:10:49 GMT
ENV JAVA_VERSION=17-ea+12
# Thu, 04 Mar 2021 01:11:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='e281f7d1fd2aaa858b02d5be451c51a9ed836c78d002cb82b114e6c36041eebf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ae713390655d0cfd8302cb2c840553404a3e366162ba5b9a2410ea7b6f1c27'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 04 Mar 2021 01:11:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da6ef06bd6983a3815530ecb4b6d3bcef6c011f03daa80be12f60c382e0c23e9`  
		Last Modified: Fri, 12 Feb 2021 01:01:42 GMT  
		Size: 48.9 MB (48854102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2cbabffc67d7d6521300614c7fd34cc6a54a4697d98c388898fc060b0f77d3`  
		Last Modified: Fri, 12 Feb 2021 01:26:00 GMT  
		Size: 16.5 MB (16465019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9e797072c5a62d6c1d30452cea11e0d4e878f3baf6d61175f1807a2d552c49`  
		Last Modified: Thu, 04 Mar 2021 01:17:44 GMT  
		Size: 181.7 MB (181733684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
