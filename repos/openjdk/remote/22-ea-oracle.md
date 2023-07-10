## `openjdk:22-ea-oracle`

```console
$ docker pull openjdk@sha256:6497046be05dbcc906c4f5841e94c472daa790a718e1df96e47d1217de789ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:0422fec8e1032882386aa9509badd788bf2c7a09d537961227759da4e72d8f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264546489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fd3aa3243706ede20966ab66c3f81fc942f2322b81e39f09deffa731e97641`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 02:04:16 GMT
ADD file:7a7c6d19e1a4f691c6bd96ea6b7568f6cc041fce11298e57d51913b978e9e7e3 in / 
# Tue, 04 Jul 2023 02:04:17 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 17:47:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 04 Jul 2023 17:47:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 04 Jul 2023 17:47:25 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 17:47:25 GMT
ENV LANG=C.UTF-8
# Mon, 10 Jul 2023 20:46:35 GMT
ENV JAVA_VERSION=22-ea+5
# Mon, 10 Jul 2023 20:46:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/5/GPL/openjdk-22-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='64f27322499a7876328a444330c8a1c5ff621b3db22129d046b7e8c2e8451e3a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/5/GPL/openjdk-22-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='4a0df847d4239efb0ea7c9a05fcfcc0f2205acfeb6628f9df38f4775d7ad9fd1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 10 Jul 2023 20:46:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2c03c89dcad02e83fe01768b82c438fcf60b831104614ca96ed5d8df01db295`  
		Last Modified: Tue, 04 Jul 2023 02:05:27 GMT  
		Size: 44.9 MB (44876686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1589371ef7dbf0bbba39e839420d2a593e729690f3c9a3a1cc86d3cd6b47912`  
		Last Modified: Tue, 04 Jul 2023 17:50:16 GMT  
		Size: 15.0 MB (14998167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279a9e3c48b532e1a37d5c5cdb7dbc5708d6a6828d007118e72a986a393add30`  
		Last Modified: Mon, 10 Jul 2023 20:51:03 GMT  
		Size: 204.7 MB (204671636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:50c92674482d209f23a808c367564a2a1430c202091386f993013c0c94251c79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262268808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ceba5a1f24e446533bd5953a8713416f26b40628f66dd465d36e142f78d168`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 00:52:20 GMT
ADD file:1313260ee8b32fa94bcf06c44034cd7e4f9baf44c7df9e74facfe21323b37292 in / 
# Tue, 04 Jul 2023 00:52:21 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 01:17:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 04 Jul 2023 01:17:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 04 Jul 2023 01:17:21 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 01:17:21 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 01:17:21 GMT
ENV JAVA_VERSION=22-ea+4
# Tue, 04 Jul 2023 01:17:30 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/4/GPL/openjdk-22-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='111b948b388db6860600e818e37829ff19879485028ba8cf17540ce995a34f47'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/4/GPL/openjdk-22-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='69ecb18f5d29ab95fefcbb70d7a1a4c7059383e949e8c44b95c08240f56fcd18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 04 Jul 2023 01:17:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29e800056b7e3d5007df41c0ad55416bb45d5863affcf39316c5755e71b20a30`  
		Last Modified: Tue, 04 Jul 2023 00:53:16 GMT  
		Size: 43.6 MB (43595268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e6eec249ed9ec194f18c4c5eda620b32132cc41a2083ec5505ff863774f15`  
		Last Modified: Tue, 04 Jul 2023 01:21:26 GMT  
		Size: 15.7 MB (15676974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b91b9babde351c99ca98df89abb6e946885e0ec6aefc34b84377ff364972c5`  
		Last Modified: Tue, 04 Jul 2023 01:21:37 GMT  
		Size: 203.0 MB (202996566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
