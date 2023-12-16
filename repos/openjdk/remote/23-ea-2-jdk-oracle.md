## `openjdk:23-ea-2-jdk-oracle`

```console
$ docker pull openjdk@sha256:0401622b545a09bb226edbc86fb436617341f8c4cb058d8e6a541b7ac0fd173f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-2-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:bfacbf6914020e0074b2ec76f0ffee6aab9700fc6a3a51c7fa8b16d77a856bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269278399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e026b4fea8d97c1a7368b893263669e2d142f3509e2b68694e9836c7a95ac83`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Dec 2023 19:23:17 GMT
ADD file:0fefdd26d1656281881908973318cde9ebc07674dc1098bbf40d9ce6acf2f036 in / 
# Wed, 06 Dec 2023 19:23:18 GMT
CMD ["/bin/bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9f2695d7e5b00c4289ec17d08776fb4b6664a9c805294c7d5c364b56d3b9435`  
		Last Modified: Wed, 06 Dec 2023 19:24:28 GMT  
		Size: 51.3 MB (51319965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b50b646c649fd0100ff8e093760c71fafb17c17ce4db0983c0e19a5cd0af9a`  
		Last Modified: Sat, 16 Dec 2023 01:52:10 GMT  
		Size: 15.0 MB (15003818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401397eb7d249e669ee7e8502f1c7646790132003d9580084c2fa590d9cd4e9f`  
		Last Modified: Sat, 16 Dec 2023 01:52:15 GMT  
		Size: 203.0 MB (202954616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-2-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c9afd03b7dbd00357c815f3b0144a421248f8fbed2328ef15fa217f15f7e6135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8914f5144b57a574c911658b91f974be4d1702abc7fb3a305b597106387471`

```dockerfile
```

-	Layers:
	-	`sha256:7e20e0033e542e5c7a59d0278b5c18a5a287a78c3921806868b48b7db8830f74`  
		Last Modified: Sat, 16 Dec 2023 01:52:10 GMT  
		Size: 1.9 MB (1915813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76d698bb8f1542611cc27191c08f772a777895c17db684344075bdca4b932b0`  
		Last Modified: Sat, 16 Dec 2023 01:52:10 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-2-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b42e80447636e70920beec9554225c24d3b0820f421a1ce25ba6ecf388088dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266620858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95035d7fedf3933f2eab3b584243db03aae2c77b9c80ef373d1cbeb03104f4a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Dec 2023 19:42:27 GMT
ADD file:f5ee75151bd25b33e72aa4c0560815f35f6e662876bf3733a02e5cb970227358 in / 
# Wed, 06 Dec 2023 19:42:27 GMT
CMD ["/bin/bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:edfaa6c9daada52a737333e0818f3d697d745aab3f3351e773218a524ebc9e53`  
		Last Modified: Wed, 06 Dec 2023 19:43:23 GMT  
		Size: 50.1 MB (50072545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61733c769b5e0a95819f0df3a4ff8980287c816c785b828bfb4321091a36b7f5`  
		Last Modified: Fri, 15 Dec 2023 23:19:58 GMT  
		Size: 15.7 MB (15686550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ccedffc6e6f877ccd22b7130dfd06f27fbee00b306cc91f823faff20d32ac`  
		Last Modified: Sat, 16 Dec 2023 09:26:47 GMT  
		Size: 200.9 MB (200861763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-2-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f904f1841ac7ad9a2040e096dd4e9e4e71b3f685b4f63e05ab304d5a437f534e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8ac3121f8685045a56d745d9080b2d61281a3936955b195cd95db0b9699bea`

```dockerfile
```

-	Layers:
	-	`sha256:4474043a7ba0333b72aed93140e7498e24d62ee0c9d7dd6b6b4bb0bafa61808e`  
		Last Modified: Sat, 16 Dec 2023 09:26:42 GMT  
		Size: 1.9 MB (1914393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29f44cd24ff101b1336e6763083ec631f5962c610204fad4f4e0fd82de3b812`  
		Last Modified: Sat, 16 Dec 2023 09:26:42 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.in-toto+json
