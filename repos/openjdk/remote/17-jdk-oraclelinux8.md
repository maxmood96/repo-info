## `openjdk:17-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:67b9a41853566e55548e2cfd119d672606893956610b44ab02e4347c847298f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d50104b0b5811b60c198a3e5ced23c783a49e0d4f78b99762fca4bfdbbc59dd2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242600352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98edbd09d5e6bc1619417d5960ca54640fba032fb6045912e42397a1661eb225`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 16:28:05 GMT
ADD file:99c665dc5bddb30b592aa86f66d1256f41b468201a93afe0c6164edb42c388c4 in / 
# Wed, 29 Sep 2021 16:28:06 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 16:53:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 29 Sep 2021 16:54:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 29 Sep 2021 16:54:56 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 16:54:57 GMT
ENV LANG=C.UTF-8
# Wed, 29 Sep 2021 16:54:57 GMT
ENV JAVA_VERSION=17
# Wed, 29 Sep 2021 16:55:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Sep 2021 16:55:08 GMT
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
	-	`sha256:c3ac52a47b61b054c43e9e9445166aedd9fa437b576839677e6fe30e0894fdc9`  
		Last Modified: Wed, 29 Sep 2021 17:04:24 GMT  
		Size: 187.1 MB (187146656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ca41f2f95a3c46087d4a3cd075293ed3e0d43c2784a695047140a15367de1de9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242110780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724a1babe7301d013c730002ad3e3faae1599a16e82e0d2f3699f18a89d4f79a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 09:28:21 GMT
ADD file:19a29c4f8accf14e581617044399a0a04fbdf31b2a3dd531b59c72d011deea65 in / 
# Wed, 29 Sep 2021 09:28:21 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 10:13:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 29 Sep 2021 10:15:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 29 Sep 2021 10:15:26 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 10:15:26 GMT
ENV LANG=C.UTF-8
# Wed, 29 Sep 2021 10:15:26 GMT
ENV JAVA_VERSION=17
# Wed, 29 Sep 2021 10:15:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Sep 2021 10:15:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fbe1b66208e55e97b0e90b882e6fdeed78abb9318897a2d87343840b78e723ef`  
		Last Modified: Wed, 29 Sep 2021 09:29:46 GMT  
		Size: 41.9 MB (41883345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fe2b96b9211b7b369c53846fe42fa00426fa23a6d736fb50873c69ffc8b3c9`  
		Last Modified: Wed, 29 Sep 2021 10:29:47 GMT  
		Size: 14.3 MB (14275215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a8cdcb505287640d48dd3ff6a0acd028182ef15adba7e1b20289cc828fbac8`  
		Last Modified: Wed, 29 Sep 2021 10:32:06 GMT  
		Size: 186.0 MB (185952220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
