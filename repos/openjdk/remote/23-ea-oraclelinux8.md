## `openjdk:23-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:bb9ee0e0e8af747663bb4306acbe5c5d13fc2c6c59eb6c22aa8667914fca91b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:9b0191353c1182123f4c1f8b1f5e8a6a8deb0bf493009a51351b9b4e49c3ca39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277179309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edca1047e842a5d024d1d28b3cb329e715ccfabbc218f3480d52d132f2b253e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:38 GMT
ADD file:84af894fe0d5a8bb12f40298f9f335a32690ab134479a6ea30fcc2bc26a26ef1 in / 
# Fri, 05 Apr 2024 18:23:38 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ba873cb070a415e56d6738ae3d788d885c6c5f1ff7e83f992de040a8e758b46`  
		Last Modified: Fri, 05 Apr 2024 18:24:46 GMT  
		Size: 51.3 MB (51318108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507b0eb4e1c25bb437ae1c7681387b72f10cbf41be071c7a462daee6304baca9`  
		Last Modified: Mon, 15 Apr 2024 17:51:00 GMT  
		Size: 15.0 MB (15008375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ecf24b7984df5ebc6d5ccd67a3a8f9960df3045de468aff37a9170d74f1e2d`  
		Last Modified: Mon, 15 Apr 2024 17:51:04 GMT  
		Size: 210.9 MB (210852826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6dccdb21702b7adfb6971dce1b863410df4aa8c06b44220799b68f7bcbd602f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008ed8c393bc85ee5efd04b60a77b9490d3b765ce5e067a07d652d1130b057c0`

```dockerfile
```

-	Layers:
	-	`sha256:7468b07d129811311b4d70bbc0619f8c70c4ca1297faf53e88ef8026f055a063`  
		Last Modified: Mon, 15 Apr 2024 17:51:00 GMT  
		Size: 2.3 MB (2267540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ef7c4c80a3efd4490d34317451b2d4ac031d99cec62be10ac6d05e4aeeac09`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e929bb9bbec0b359ed8c90ced4ba2e720d057d4a762f2d9c664ecaa729e971b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274526507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2596bc41392ba35fcd944c39a2f182ac5de7dd88687dda46efd9220a2ca3949`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 05 Apr 2024 18:10:10 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Fri, 05 Apr 2024 18:10:10 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b0617b3cebc152b6696d41bbdefba8666a2d9eaec7ad732753d8c4e95fe9118`  
		Last Modified: Fri, 05 Apr 2024 18:11:06 GMT  
		Size: 50.1 MB (50085033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd1c95675309ba61695d4766737254988792b031a16cffd9d95f2f37bedd392`  
		Last Modified: Fri, 05 Apr 2024 19:11:16 GMT  
		Size: 15.7 MB (15706096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26610132a57b289a80723354dd2093814257cf7b5cf449887b1f5c7fea29957c`  
		Last Modified: Mon, 15 Apr 2024 20:20:21 GMT  
		Size: 208.7 MB (208735378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5fe84623aa7f3d3ff727b8ccedec6d632741e1888a7758cfe33826ccc78e3af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31aa49c2b447a7ac21bdff087d65447088630cdb66bf3203a2d307dd6fabf56`

```dockerfile
```

-	Layers:
	-	`sha256:20ff02f05bcd5c9387e70d2a912d23fff524f4d5dbe7f009c8f76f68f7519ef7`  
		Last Modified: Mon, 15 Apr 2024 20:20:17 GMT  
		Size: 2.3 MB (2265984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b8aa55bb6dd1207bbde914b566ed40aee183fa2221a5fa7c1713e657dee2cc`  
		Last Modified: Mon, 15 Apr 2024 20:20:16 GMT  
		Size: 16.0 KB (16028 bytes)  
		MIME: application/vnd.in-toto+json
