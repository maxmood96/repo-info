## `openjdk:20-ea-14-oraclelinux7`

```console
$ docker pull openjdk@sha256:7ade6e2c768a0c72d3a139d461c13c401f9c8e36d330775b75d597df467c767a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-14-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:735d346c5d6448764384b530265dac239e1ed034fa12244cd01e26cc5814bef4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259803726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670938e52e7a872b8e7299cb37c022a2fc4ec5ca2821791b0b4551285a28ab06`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:42 GMT
ADD file:adf7ebc1d65494dba22f4f0a12f2f8f63128836b87646ffd6e9964f936343e6d in / 
# Wed, 24 Aug 2022 19:35:43 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 22:44:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 24 Aug 2022 22:44:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 24 Aug 2022 22:44:32 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:44:33 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Sep 2022 22:36:00 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 22:36:13 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='ce9c99a0d70bf7c6548b68a33770a50d1273d5d5ea72522a1fe91ae6d3f22c1d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='4935236eb4e51be13ddfcc1ce717191128feb8ff9329676971ea54775261d9ff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Sep 2022 22:36:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9815334b7810943f0c417fa41a2732d56b098252185c5749c2c2ce80f8e8e140`  
		Last Modified: Wed, 24 Aug 2022 19:37:41 GMT  
		Size: 48.7 MB (48727120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbb6577271d2ea4eb7961ad553fcac407890cd27f6514b5d071119191d585fd`  
		Last Modified: Wed, 24 Aug 2022 22:49:44 GMT  
		Size: 14.2 MB (14230815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b45dfc1330925fe66c54a9cbe14bc6a251f274ac40bb9b998c865ca9d7341`  
		Last Modified: Mon, 12 Sep 2022 22:41:27 GMT  
		Size: 196.8 MB (196845791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-14-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7ac7318221f9d969ff38a75714d42e1b031ea80e9fae4d278923b1ae2ac59366
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.9 MB (259936183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e876e75a24433aac25e003be1ee46241aae96f713d4107cb678bf46c9f95d4a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Aug 2022 19:55:21 GMT
ADD file:58b53a780a05a9f314e6821fd85f38a0d86fed5a98ab7c3fd52b0ea2341c3d64 in / 
# Wed, 24 Aug 2022 19:55:22 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:31:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 24 Aug 2022 23:31:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 24 Aug 2022 23:31:55 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 23:31:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Sep 2022 23:04:23 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 23:04:41 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='ce9c99a0d70bf7c6548b68a33770a50d1273d5d5ea72522a1fe91ae6d3f22c1d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='4935236eb4e51be13ddfcc1ce717191128feb8ff9329676971ea54775261d9ff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Sep 2022 23:04:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d094a37c2b34cb4c876f39d579c422eba5a195ec17dff5a5fcbbbd9398dafef`  
		Last Modified: Wed, 24 Aug 2022 19:57:30 GMT  
		Size: 49.3 MB (49309770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346cd8d935004b602845ed18ab7ddf7b6bf15cfcb9eb50d1b98f6153c188f3a3`  
		Last Modified: Wed, 24 Aug 2022 23:41:46 GMT  
		Size: 15.3 MB (15266557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6221434c35c5c305ce5845e1431d0d887e9fd247baaae7bc0071b88417f0d95`  
		Last Modified: Mon, 12 Sep 2022 23:13:56 GMT  
		Size: 195.4 MB (195359856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
