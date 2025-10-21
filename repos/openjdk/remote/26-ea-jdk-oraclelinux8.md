## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:e8f846e61629bff8eea4366a0ce41e716b5367f79b8eaf6bf8933d88166bfdce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:5f49dd1483b0375dc78bebe79f04edfd4703c4ee0b6cf7a3a68458c47adeccc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292475361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119c55ae47907713ac7ac4e192e96ced4ba4a1e7112803446355ee8782e1e272`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70e7deeb6fb1025fbac694ef1855ba75493ab45e96d46a5423af063e321cfd2a`  
		Last Modified: Tue, 21 Oct 2025 00:13:40 GMT  
		Size: 51.3 MB (51317328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a219360f10113719273ca545b8be6b48874fe642761259bbefcddca6f7e96c`  
		Last Modified: Tue, 21 Oct 2025 00:21:47 GMT  
		Size: 15.0 MB (14988872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e961a33aea2e565fd923f1c79a0d36824f9a9dd4ee1f0115602d983b3cec977`  
		Last Modified: Tue, 21 Oct 2025 03:31:43 GMT  
		Size: 226.2 MB (226169161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:bc61b98e201194fa1c612f1ff1a4cdab369af8ea903d29faccfa4195e709a1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4db7ae21a9dd0578df205ab12c78c01b07880d4b53b5208a3b9343ac9dea64`

```dockerfile
```

-	Layers:
	-	`sha256:8b7dc8739fffa692ddcd60bb4d04d3da3a6a608e793664a22516d3f756f898f6`  
		Last Modified: Tue, 21 Oct 2025 03:23:24 GMT  
		Size: 2.5 MB (2451129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c513319e329fc5067b7d08e318a73f642ffa1be0bdf44e50cfb6a36b8cdeec1b`  
		Last Modified: Tue, 21 Oct 2025 03:23:25 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:188e28b5445e769ea487a8258aac2eff035a0088bd557f199aa97deee948f5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289731883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53901b9e5d1a0fe019601480aecea178157ceed60c3d42ab2ff9883c071d841c`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb2cbf1306f13796052df61db1ffdb76b5d1db3837223eec0859c6a0d6f6cdff`  
		Last Modified: Tue, 21 Oct 2025 00:12:37 GMT  
		Size: 50.0 MB (50043445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476ed5ae14d85c1211f4736c7e8a770b23a9a21a347aa23c35bac1699dbabc1`  
		Last Modified: Tue, 21 Oct 2025 00:25:16 GMT  
		Size: 15.7 MB (15663340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf014d8657918ad0d996335850dec7d22a1de99c7352505db2a6155635a3f914`  
		Last Modified: Tue, 21 Oct 2025 02:55:13 GMT  
		Size: 224.0 MB (224025098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:576f61a623ca065c138d8a4936f5018f1221be261ea52310c43259cdfd254119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f308022e79109dbb95525fa0d3939ba8b9bcf85cd9a025a510f07ce66b5b1c5`

```dockerfile
```

-	Layers:
	-	`sha256:11db1db8d8f38cb02bfd85560c5f7ef1649f9e9374ee5edd83a4965a52e7f69b`  
		Last Modified: Tue, 21 Oct 2025 03:23:29 GMT  
		Size: 2.4 MB (2449963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af57390e70ca3345017c644510e8644c50e88eaa9e488ec7eeaddced80a58a28`  
		Last Modified: Tue, 21 Oct 2025 03:23:29 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
