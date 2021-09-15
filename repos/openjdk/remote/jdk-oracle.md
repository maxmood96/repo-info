## `openjdk:jdk-oracle`

```console
$ docker pull openjdk@sha256:a51d9fb4a310a1fbbd1bdc2138e04a13631ab83db432214c813f09d578a54a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:9f507a555448a8bdaa3c85f63c4e693e13e74a93a034803af7498f1d992dd3f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242678037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff693b5bd1bb25516b3b8df5d9140031551bdc9215b52b0f404313b5fb1824b1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Aug 2021 19:20:55 GMT
ADD file:ab982d6f37710c434f7ef9650c722d3c6333906cbb9344bf91e79068088bcc69 in / 
# Thu, 12 Aug 2021 19:20:56 GMT
CMD ["/bin/bash"]
# Thu, 12 Aug 2021 19:37:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 12 Aug 2021 19:38:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 12 Aug 2021 19:38:25 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Aug 2021 19:38:25 GMT
ENV LANG=C.UTF-8
# Thu, 12 Aug 2021 19:38:25 GMT
ENV JAVA_VERSION=17
# Thu, 12 Aug 2021 19:38:37 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 12 Aug 2021 19:38:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c67289558ae5eb060942db5bf46d182448587a87e21c680a0486b147d4b9a0b4`  
		Last Modified: Thu, 12 Aug 2021 19:22:09 GMT  
		Size: 42.2 MB (42158041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12787f1f3888c64bfc9e779a9705ecc45ae1a60b3757074b6f16cf1d8553cac8`  
		Last Modified: Thu, 12 Aug 2021 19:43:29 GMT  
		Size: 13.4 MB (13373335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b68cfe81aec89c9ea5d63332c1b03b8ceff1475a26ea818f01a9f09e15ed95`  
		Last Modified: Thu, 12 Aug 2021 19:44:41 GMT  
		Size: 187.1 MB (187146661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4fa3065dff06d89784ff5d178e59a79de36f8ef5a3aa2ab2986b13365ae503d8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242170072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007e7bd8d4f5dd87b09c0748703c27ad640173539bc79e37e0d72e5ba207c4c0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Aug 2021 02:58:07 GMT
ADD file:3a5bc6124c8d78438880a95007baec403400e29f09317331e09ba7d65a0aaff0 in / 
# Fri, 13 Aug 2021 02:58:08 GMT
CMD ["/bin/bash"]
# Fri, 13 Aug 2021 05:39:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 13 Aug 2021 05:40:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 13 Aug 2021 05:40:57 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Aug 2021 05:40:57 GMT
ENV LANG=C.UTF-8
# Fri, 13 Aug 2021 05:40:57 GMT
ENV JAVA_VERSION=17
# Fri, 13 Aug 2021 05:41:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Aug 2021 05:41:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:757bb77daa0e625f3aaa9e22fcc2dda31fa9d6e50f482403ab7be9f030a1a19f`  
		Last Modified: Fri, 13 Aug 2021 02:59:14 GMT  
		Size: 42.1 MB (42054178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d701f3bd7e43b3fb331b6b15362e9dbd4abd27a5c29f2301d998cc782a0ba1`  
		Last Modified: Fri, 13 Aug 2021 05:50:47 GMT  
		Size: 14.2 MB (14163676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c27a06b1372926a2a3b345e6c84560e90c58b547b4ab84a8f47d8358647eed0`  
		Last Modified: Fri, 13 Aug 2021 05:52:21 GMT  
		Size: 186.0 MB (185952218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
