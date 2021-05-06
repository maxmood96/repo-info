## `openjdk:17-oraclelinux7`

```console
$ docker pull openjdk@sha256:e4c79aab232e5bc81a08765a4e26da3e229aa77869051da901bf27452fdbcf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:eadbffc95ff573d736f598282e5264c10ed1b5f8b36aa347cbf8644d7dedf306
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249685890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68a0a6ce2177ee8b027d9b4b8c29aa6459e62c1b7aa0e71dc5ae6e7bba78b73`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 May 2021 00:10:37 GMT
ADD file:7532c4c6850a2e95d341f39828f60573728d50ba1fc6264ed19bb36eb4b24d1c in / 
# Thu, 06 May 2021 00:10:37 GMT
CMD ["/bin/bash"]
# Thu, 06 May 2021 00:27:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 06 May 2021 00:27:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 06 May 2021 00:27:43 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 00:27:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 06 May 2021 00:27:44 GMT
ENV JAVA_VERSION=17-ea+20
# Thu, 06 May 2021 00:27:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/20/GPL/openjdk-17-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='2de5c546c3e38f36676c7e22dd040e5b540fc258f72194e7ae17af3f2bf7f0b5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/20/GPL/openjdk-17-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='9e376a3f2c9a3dc5394fc2f3da480f72b9103c3b71d39d041dc6b08bb65e5724'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 06 May 2021 00:27:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:22f7711cf64307564c3293688489295d9458bac2ca47cd6576382cfb75c9d2b9`  
		Last Modified: Thu, 06 May 2021 00:11:49 GMT  
		Size: 48.3 MB (48258661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87180291cc45c5c610f6909495ba989b36ef14701a331d8689e264f9d7c23796`  
		Last Modified: Thu, 06 May 2021 00:32:56 GMT  
		Size: 15.4 MB (15423518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01275d48e1e68d6ac23761ed472996680a58280ac8dd3153ac9afe19b4a03ed`  
		Last Modified: Thu, 06 May 2021 00:33:12 GMT  
		Size: 186.0 MB (186003711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e469732cca3709dfa9149c5fd6f06e6085dbc26d7a0fc481a44a47a68c9e166f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247424258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3c9db3b42c9502e62501336d53a7b46533f27f13c1814c3314afaee801b0be`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 May 2021 00:13:32 GMT
ADD file:57303578fa11d312dcc51eb7aef116316c2b60e48b533a1471e2f2ba915ee46a in / 
# Thu, 06 May 2021 00:13:35 GMT
CMD ["/bin/bash"]
# Thu, 06 May 2021 00:32:13 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 06 May 2021 00:32:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 06 May 2021 00:32:15 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 00:32:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 06 May 2021 00:32:16 GMT
ENV JAVA_VERSION=17-ea+20
# Thu, 06 May 2021 00:33:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/20/GPL/openjdk-17-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='2de5c546c3e38f36676c7e22dd040e5b540fc258f72194e7ae17af3f2bf7f0b5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/20/GPL/openjdk-17-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='9e376a3f2c9a3dc5394fc2f3da480f72b9103c3b71d39d041dc6b08bb65e5724'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 06 May 2021 00:33:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d575bf1166e11ab792c567b7bdfab507a987976bc375994e3516987e6e1e600`  
		Last Modified: Thu, 06 May 2021 00:14:38 GMT  
		Size: 48.9 MB (48869643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7892e1551bf2c1decd5f1f367d2f9dbf15317e29aa12b267cf59b9c255a91b34`  
		Last Modified: Thu, 06 May 2021 00:39:13 GMT  
		Size: 16.5 MB (16472243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf66c7eb878c2a9d9945e5c001ff27044631254190716ab021156a0027b0e435`  
		Last Modified: Thu, 06 May 2021 00:39:33 GMT  
		Size: 182.1 MB (182082372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
