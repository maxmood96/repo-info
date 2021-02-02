## `openjdk:15-oraclelinux7`

```console
$ docker pull openjdk@sha256:786b4f77dff488fade893cfff225cfd0c7f8476b1d06ff2d54d748510c293ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:ceae21695c60efd5d68dc1c03bee442a9ce29135a6867455983b9b943ffbd2e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259499671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1deea23bad79642801d8c26cd3ff94178fc92c311d77a043615cb5b3b8f7be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:48 GMT
ADD file:430ae887b8a202818526e7c39819c089bee09a496bbd4cab85759814c30dde4b in / 
# Mon, 01 Feb 2021 20:32:49 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:55:53 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 23:59:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 01 Feb 2021 23:59:19 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:59:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Feb 2021 23:59:19 GMT
ENV JAVA_VERSION=15.0.2
# Mon, 01 Feb 2021 23:59:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='91ac6fc353b6bf39d995572b700e37a20e119a87034eeb939a6f24356fbcd207'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='3958f01858f9290c48c23e7804a0af3624e8eca6749b085c425df4c4f2f7dcbc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 23:59:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69d77e45731bec64e61a0f08021494f9c0f93a8dc00071bebe5ce614dec1f72a`  
		Last Modified: Mon, 01 Feb 2021 20:34:46 GMT  
		Size: 48.3 MB (48263590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5df3ce42f8a33f03c8ac097c0e1adc969007d8424ef47e9b638a58b42e82a6a`  
		Last Modified: Tue, 02 Feb 2021 00:04:46 GMT  
		Size: 15.4 MB (15437017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134dabdfc154546938b729a8281f0692e4e7a9a1d853ea54586ab5063429a6fc`  
		Last Modified: Tue, 02 Feb 2021 00:07:16 GMT  
		Size: 195.8 MB (195799064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:341489e7d7b866b48301ba9fba9d3fbaea9911c1fb1cbf5d4edb19e805e26a24
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240199926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06742c75521578c011a3900b253853ed181e897ca8e8adc8fd04a19ebd1fc4e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:01:37 GMT
ADD file:515797e9c94114d9811e4f5e7ef89e24a7c02f5496694320cf17c5b2c2c62577 in / 
# Mon, 01 Feb 2021 21:01:39 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:07:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 21:11:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 01 Feb 2021 21:11:20 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:11:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Feb 2021 21:11:21 GMT
ENV JAVA_VERSION=15.0.2
# Mon, 01 Feb 2021 21:11:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='91ac6fc353b6bf39d995572b700e37a20e119a87034eeb939a6f24356fbcd207'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='3958f01858f9290c48c23e7804a0af3624e8eca6749b085c425df4c4f2f7dcbc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 21:11:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:679e771030bbd97d6d7a7cf8b0a2290601de0b646eaa29d88c48562a70464c12`  
		Last Modified: Mon, 01 Feb 2021 21:03:42 GMT  
		Size: 48.9 MB (48851459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff96049663e262709e8d337b37d084629a90f0707979070456acf5338444948`  
		Last Modified: Mon, 01 Feb 2021 21:16:24 GMT  
		Size: 16.5 MB (16466150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2cae8da722b16133acf6247ac0697c0636aed1c6d4fe0d31909a902c60032`  
		Last Modified: Mon, 01 Feb 2021 21:19:38 GMT  
		Size: 174.9 MB (174882317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
