## `openjdk:19-ea-13-oraclelinux7`

```console
$ docker pull openjdk@sha256:086bf366abdcc80e1de9373d8fab1ead75d4af95cc4e9ca1ff066154b2b88661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-13-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:f857b5582f69774a6ccee80fdbeac87b5b065ac8f710d352b52c29c370b458dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256814892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62a143fde45123843895a8b50df6db1dad25e64b003b85f0546f8c88f920a7e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:38:09 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 25 Feb 2022 03:38:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 03:38:10 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 03:38:10 GMT
ENV LANG=en_US.UTF-8
# Mon, 14 Mar 2022 20:14:24 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 20:14:34 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 20:14:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a747076cd653f857a43ad06edf375d2d7f9d70470d618d826d9fd2239d9431e4`  
		Last Modified: Fri, 25 Feb 2022 05:32:07 GMT  
		Size: 15.4 MB (15402277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76562cf67d9a017157be6ade78bc970c677b7984f1733e88d838e0ac9765199`  
		Last Modified: Mon, 14 Mar 2022 20:22:27 GMT  
		Size: 193.1 MB (193081753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-13-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8ac6416c1946add3be8d1eff0e345f067ed16fa812242875a8e6718f0c5f5ec3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256733083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b6d961c157a685571c866b3e1907a7545db23e849c908d03565f59e4d772c3`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 19 Mar 2022 01:00:51 GMT
ADD file:a5f18f088f362b979701dd9843b784391fd01ee9f85e19b4a66089ccba650d8a in / 
# Sat, 19 Mar 2022 01:00:51 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 07:23:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 19 Mar 2022 07:23:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Sat, 19 Mar 2022 07:23:17 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 07:23:18 GMT
ENV LANG=en_US.UTF-8
# Sat, 19 Mar 2022 07:23:19 GMT
ENV JAVA_VERSION=19-ea+13
# Sat, 19 Mar 2022 07:23:37 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 07:23:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:141b1a23f5c914f6ea3d33bbb54ee6e46d83e342a4f16e079f825362e6db5a24`  
		Last Modified: Sat, 19 Mar 2022 01:01:46 GMT  
		Size: 49.3 MB (49339592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcf257e8020deec6d6f5ad76b9c36d1eca4b42e96527feb4c52735766f320b7`  
		Last Modified: Sat, 19 Mar 2022 07:44:40 GMT  
		Size: 15.3 MB (15278942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231f0875a1044887aa2b4e740edf1ea71c499c45a994cac3621964ad86e17799`  
		Last Modified: Sat, 19 Mar 2022 07:44:57 GMT  
		Size: 192.1 MB (192114549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
