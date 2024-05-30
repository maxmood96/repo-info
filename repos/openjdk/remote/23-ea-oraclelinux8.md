## `openjdk:23-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:e30a7cf051b3191947ba2c976ce8717accc496e1f1c0cdb6c5169a93a248016d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:5add1add8a2feff70ee77bc8db6a09e7df03d3f5687239ba3852d59af57a4a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277274793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0544eccf02d53ccbb51979cc43f7e6f54b409ee9a009a9fc85e0e42b3ab51bc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:30:46 GMT
ADD file:4ff19cbeee6ebf4bee966dae7b731f4e3b438445f959c2d77b362e6db8e75ece in / 
# Thu, 09 May 2024 22:30:47 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 29 May 2024 17:23:46 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 29 May 2024 17:23:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c51d994efc098621a8777bd1a698f8e622b9ded5d362c17301551077048d589c`  
		Last Modified: Thu, 09 May 2024 22:32:36 GMT  
		Size: 51.3 MB (51320982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4d3ec3d1be833d161d8912d47a0e9706975539ac7acb2acfe71a93439b35ea`  
		Last Modified: Wed, 29 May 2024 23:01:38 GMT  
		Size: 15.0 MB (15015851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2490dd590b9cbaa68a0d4e6d4c47afec15f3bec5bf3fda659e6b2633cde38f70`  
		Last Modified: Wed, 29 May 2024 23:01:42 GMT  
		Size: 210.9 MB (210937960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9ece47efa3738f9a528846695226a267a02235bc451860929e79c3993cedbfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0155599a5891e149617863cee024e1cdd1efae87bac1b8ae96c110b61ec6b151`

```dockerfile
```

-	Layers:
	-	`sha256:a6d7d84dda271d170e6e618b33159e146b285110861e59f0b8f48c38e1eec402`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 2.3 MB (2267587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6deddbe7045b44eb50c661d26e1c0489a95ac351b6597112550d1f3c2b8e496e`  
		Last Modified: Wed, 29 May 2024 23:01:38 GMT  
		Size: 15.8 KB (15771 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:76fe6d7edcb63c483eb9149ec004205d69c1210139260f08ca81f9588d48bf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273409030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d69a8707fea919d03a2f17b9335b1f453a1a1dc2aedc19fc6dfabf0bcc308f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:06:44 GMT
ADD file:603b84a8cdf20851437bb944c9946c0ac32645e0e0946ffebf3ed5ad10c141bc in / 
# Thu, 09 May 2024 22:06:45 GMT
CMD ["/bin/bash"]
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 17 May 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+23
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='ebb29aa3b7c39ccf29ce564c797c5723b7355880f5dafd239570f7e7f2166bfe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='feef29529ab1660b95345ebbc6f47ba2823e28e87596225a25d2c45fc4537f29'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 17 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8999f2c02994f155685ddf5b1c0822a620022aa57946ee7ba5c754261052b2dd`  
		Last Modified: Thu, 09 May 2024 22:08:16 GMT  
		Size: 50.1 MB (50082252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2621a0b881622f503ff8b218af9315ee5ba6b65472e45dd71e10ecaefc2a5cfb`  
		Last Modified: Fri, 10 May 2024 00:16:40 GMT  
		Size: 15.7 MB (15699035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a607340b56dee7a23623ec22e27b666d3d889865ab63bdbd26a593ed23c46354`  
		Last Modified: Fri, 17 May 2024 19:45:55 GMT  
		Size: 207.6 MB (207627743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:eb0037664aacdbcadd24c261110c9929634ab49dd9ec73bc65588662eaedb49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10efec615801540e758d047d12a5558f7c6e29d3fc56102714db8865b9685e0b`

```dockerfile
```

-	Layers:
	-	`sha256:4a6277afa5d0938b5f3698d12dc93350d61f98eafd4c9591f9983a3ef23a1832`  
		Last Modified: Fri, 17 May 2024 19:45:50 GMT  
		Size: 2.3 MB (2266993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5eb54501b4f467abe022d52470f19a2eb1c4563d68ccac587edc33bc9f38cc`  
		Last Modified: Fri, 17 May 2024 19:45:50 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json
