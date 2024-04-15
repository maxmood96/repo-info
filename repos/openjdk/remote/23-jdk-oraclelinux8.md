## `openjdk:23-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:c7c05000040c7abaf2410158a92c5faf39cbb96d385df535a8f3c43f181ed265
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux8` - linux; amd64

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

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

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

### `openjdk:23-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:08727ad4c5eb2ddcf26e4c71976cc3536b1cf1c5da477aac1c5166f68b3f99c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274524368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e345c286cdfbf627c9979fa768d70f5b5293589888e3a1ae83aeaa586a012b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Apr 2024 18:48:10 GMT
ADD file:20c35b83c8a00616d018b5fe950bbeaed79c5f55895791872a060cfd0823436e in / 
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["/bin/bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
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
	-	`sha256:c4acd96b481794515dbc191ca4a6a3f08a669379c8512906d98b204e5360c7cc`  
		Last Modified: Fri, 05 Apr 2024 19:11:23 GMT  
		Size: 208.7 MB (208733239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:336bd59f85f9696e92d2b7683afb0e775ca30a6e7d8cc5437e91f403eebc90f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9874128b394a5e5df3fc2ab8c60341dcabdebeab4733ee4acfbf1b2cc798884d`

```dockerfile
```

-	Layers:
	-	`sha256:56db4125b30f5ba63670cdef1b3e3c93a9d56cf22403cc13336c0bb1501c35a2`  
		Last Modified: Fri, 05 Apr 2024 19:11:16 GMT  
		Size: 2.3 MB (2265984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9d60316147c958d92b9d2124706a301b3eaac63412404d1ba7ed22ea38637e1`  
		Last Modified: Fri, 05 Apr 2024 19:11:16 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json
