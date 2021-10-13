## `openjdk:18-jdk-oracle`

```console
$ docker pull openjdk@sha256:3ffbdd3328d9ad74cdb9ae701e9873c9ba85192568a40b36fb8d954e688d64f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a77a8fc9b3db349364bda29de2935477dc47e22f2a090beb72676cdeffd2993d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243314845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4527e57147a67ede6c8bf587f3ccd2934a1ecb48afb347dade5cf01113f4b7a3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 16:28:05 GMT
ADD file:99c665dc5bddb30b592aa86f66d1256f41b468201a93afe0c6164edb42c388c4 in / 
# Wed, 29 Sep 2021 16:28:06 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 16:53:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 29 Sep 2021 16:53:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 29 Sep 2021 16:53:34 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 16:53:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 Oct 2021 00:50:32 GMT
ENV JAVA_VERSION=18-ea+18
# Sat, 09 Oct 2021 00:50:44 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='425b4f9afe439b4690593e5f78e27b6687525114a66f652c285a7dcca95b1961'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='af5b0d66cf7c4f7450066fd67dbb0d48c17bcc5ab8ddb105cf7fe66176427f87'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 09 Oct 2021 00:50:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6540cb32758bf3f150d56508f216b26487b14ac6fd20b1c92f1e1c8357730ea9`  
		Last Modified: Wed, 29 Sep 2021 16:29:48 GMT  
		Size: 42.0 MB (41963002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acb1bb05d773c14486a356ac78716bf3e9e5b34aefb39b421cc776aea66e606`  
		Last Modified: Wed, 29 Sep 2021 17:02:29 GMT  
		Size: 13.5 MB (13490694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90f68fcad68d9ed9afd8b2d55b949bf9c44db01182486fa3ea8a9e0cae7c098`  
		Last Modified: Sat, 09 Oct 2021 00:59:29 GMT  
		Size: 187.9 MB (187861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bb74b5cc668b4193eb485018484c6854a85787c8688bb75bdf166e64f0f42b36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242933924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa6e33f3f99a8e361a9b00d371e0e05892a4f73d6a264c06a326b7dfe5f713f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 09:28:21 GMT
ADD file:19a29c4f8accf14e581617044399a0a04fbdf31b2a3dd531b59c72d011deea65 in / 
# Wed, 29 Sep 2021 09:28:21 GMT
CMD ["/bin/bash"]
# Wed, 13 Oct 2021 05:58:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 13 Oct 2021 05:58:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 13 Oct 2021 05:58:49 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 05:58:50 GMT
ENV LANG=C.UTF-8
# Wed, 13 Oct 2021 05:58:51 GMT
ENV JAVA_VERSION=18-ea+18
# Wed, 13 Oct 2021 05:59:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='425b4f9afe439b4690593e5f78e27b6687525114a66f652c285a7dcca95b1961'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='af5b0d66cf7c4f7450066fd67dbb0d48c17bcc5ab8ddb105cf7fe66176427f87'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 13 Oct 2021 05:59:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fbe1b66208e55e97b0e90b882e6fdeed78abb9318897a2d87343840b78e723ef`  
		Last Modified: Wed, 29 Sep 2021 09:29:46 GMT  
		Size: 41.9 MB (41883345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076e889c44db9131098a7368fb924c97ba81cb10aee46f9c273b2076baab08f5`  
		Last Modified: Wed, 13 Oct 2021 06:23:16 GMT  
		Size: 14.3 MB (14270423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1e63bd8497f289b3b1de6ec25c12956a4a6b4fc7021be732fc501b7f371e44`  
		Last Modified: Wed, 13 Oct 2021 06:23:33 GMT  
		Size: 186.8 MB (186780156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
