## `openjdk:23-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:363feda8732b2a59fd5472917b301bfd9cd2449a8005f6a29e7ba55e0d97449f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:bff44ae86ee1976c083446d5bcfc1aa67e77c051777d5e63293f60325f49c373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276078867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a206dd7e662777465e48898b4a12e6e5bfb483e42f879b0f352320d27a56489`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:30:46 GMT
ADD file:4ff19cbeee6ebf4bee966dae7b731f4e3b438445f959c2d77b362e6db8e75ece in / 
# Thu, 09 May 2024 22:30:47 GMT
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
	-	`sha256:c51d994efc098621a8777bd1a698f8e622b9ded5d362c17301551077048d589c`  
		Last Modified: Thu, 09 May 2024 22:32:36 GMT  
		Size: 51.3 MB (51320982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab80b29d053c9e1e137f4a916a11025eb57211a27098452a0c6f25c3a516acd4`  
		Last Modified: Fri, 17 May 2024 18:53:46 GMT  
		Size: 15.0 MB (15015765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5907d5a466d4e2cd38343728de29d08d5e0347974093da30319b385ac1d8c8`  
		Last Modified: Fri, 17 May 2024 18:53:49 GMT  
		Size: 209.7 MB (209742120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:070b9a8a2dfce4f162a611f3b5b940f08aa51706ad3ad04607e9b022c13cf79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a092c0d6508547a6b7b6ccaa3f1401c8a77300fbd02d5983cd3bc7a2c044a22d`

```dockerfile
```

-	Layers:
	-	`sha256:8774d0fece4f344d445c197b6f11667e2d47c0ba04abe5a85ae3055f267875cf`  
		Last Modified: Fri, 17 May 2024 18:53:46 GMT  
		Size: 2.3 MB (2267589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e0d022caf55c0c4f92b69e6ae023c2db4c4558c275ea548787d56a64b6d7a9`  
		Last Modified: Fri, 17 May 2024 18:53:46 GMT  
		Size: 16.2 KB (16185 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux8` - linux; arm64 variant v8

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

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

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
