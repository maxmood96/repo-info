## `openjdk:21-oraclelinux7`

```console
$ docker pull openjdk@sha256:d049a0d26d5f59c09421df12617533574c6371661efa3e79a8446f4d025fc347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:50443403bea8c8217f57768650c241f08187cdf477240f370580ecff50befb63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266146842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044800ba58b9edc92f13ebe305a043c11887fb82c7a157c580249d49216c6ddc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 20:22:54 GMT
ADD file:e205deb729daf99a168c27d3f97cd2b69e736fc9d4bee9ea220ec86921574a0f in / 
# Wed, 08 Mar 2023 20:22:55 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 20:54:26 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 08 Mar 2023 20:54:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 08 Mar 2023 20:54:26 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Mar 2023 20:54:26 GMT
ENV LANG=en_US.UTF-8
# Mon, 20 Mar 2023 23:52:58 GMT
ENV JAVA_VERSION=21-ea+14
# Mon, 20 Mar 2023 23:53:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5ff9e95f12627e7f9c4b2e61d4ddfa5eb224f6106eff7620a487244be71d9787'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='32b9ef0cafec4114aac8917e9ad754c7a3bdcfbc47143e4e5182757a0311ae66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 20 Mar 2023 23:53:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b659169cb9226d08443358aa4e8147f3144614ac33f7a41217b0cf62a4d3326`  
		Last Modified: Wed, 08 Mar 2023 20:24:41 GMT  
		Size: 50.5 MB (50467964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efc12c70e0ba49ea5eb742d598c3d36a33b4d7407f8be1a8ac8641ad14e0a56`  
		Last Modified: Wed, 08 Mar 2023 20:57:27 GMT  
		Size: 14.2 MB (14236997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58e56ee58c5d90938e3f96d6914bc958fb8ed5127960beb9c8e43f4da34f25b`  
		Last Modified: Mon, 20 Mar 2023 23:56:48 GMT  
		Size: 201.4 MB (201441881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:566c5fca1783fc4eabf3063565451eda6d9a2b69b9aa47284194d5285c65775b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266193441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51022bf87ccb9f5884b7a1074f5f0208313f318592cc933e6cd8cbedc10e055`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 21:02:36 GMT
ADD file:d11a3555d107d9db5ab5621675aa2ecf27ec872cc591769bdc75129ff602dfd7 in / 
# Wed, 08 Mar 2023 21:02:37 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 21:20:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 08 Mar 2023 21:20:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 08 Mar 2023 21:20:32 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Mar 2023 21:20:32 GMT
ENV LANG=en_US.UTF-8
# Mon, 20 Mar 2023 23:59:15 GMT
ENV JAVA_VERSION=21-ea+14
# Mon, 20 Mar 2023 23:59:27 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5ff9e95f12627e7f9c4b2e61d4ddfa5eb224f6106eff7620a487244be71d9787'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='32b9ef0cafec4114aac8917e9ad754c7a3bdcfbc47143e4e5182757a0311ae66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 20 Mar 2023 23:59:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b689a883b146569199f6bfaadce974725d68f1cd14d01950efe476637febe12`  
		Last Modified: Wed, 08 Mar 2023 21:04:11 GMT  
		Size: 51.0 MB (51027010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ce6fa2927eee2bba1cdfc5060760f859a7073e02bf271b9b61999943c2211d`  
		Last Modified: Wed, 08 Mar 2023 21:23:34 GMT  
		Size: 15.2 MB (15249325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a66e520fb7f0b086b72091bc5e9674d1fd7cee7025308cfb0b977548c5e190`  
		Last Modified: Tue, 21 Mar 2023 00:03:19 GMT  
		Size: 199.9 MB (199917106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
