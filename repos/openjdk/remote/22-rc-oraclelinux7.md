## `openjdk:22-rc-oraclelinux7`

```console
$ docker pull openjdk@sha256:3971a72fa338b604298d2e17266632eac40aae40dbbc4c800d9ee1dba9121600
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:47da0a54d9aec2489e1fdcab0f3fe5f9bd64a25b49d0f75d58a7df16a3c2f3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267389260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba71221b9cc28369b1ca9f32fdd769b4ded3cbbc61bb2a228c4c0dffb782ec`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:52 GMT
ADD file:6c43f1bc1b598f7b1a5fc6f5c7951e8525eee01704f8f5e5caec8a944a4ecb4d in / 
# Wed, 14 Feb 2024 01:47:52 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ff90099b5a4df32952d1822d472a72c931c53a68c05a3ba7431ea0f85d54135`  
		Last Modified: Wed, 14 Feb 2024 01:50:04 GMT  
		Size: 50.4 MB (50389833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d2236800381ab1d4fc5f985090876dd014aac17ed6029a121eb71ed2f99ad2`  
		Last Modified: Sat, 17 Feb 2024 00:53:46 GMT  
		Size: 14.2 MB (14231385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa667f1e0e2c52214ed7d794e92c8d0e55a50fb3c9513ba5c86b3cadfd7fba6a`  
		Last Modified: Sat, 17 Feb 2024 00:53:49 GMT  
		Size: 202.8 MB (202768042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:10b53927b3d4bbbe5b7a66b28c7814015803593d2a194f3a718315a4e90a3d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4445044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd399f954cb13262eae1fbdf72395035a594fd2ac1274e7f4ef13fda3730d820`

```dockerfile
```

-	Layers:
	-	`sha256:c6ff096d70cde417833cc968183f596245d6af052747ad233f0b9816ad074e63`  
		Last Modified: Sat, 17 Feb 2024 00:53:45 GMT  
		Size: 4.4 MB (4429245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87541d9ed3dd3b6cfce4f7b4001da5c3a17b67bf692692a7074ce6f914b1b897`  
		Last Modified: Sat, 17 Feb 2024 00:53:45 GMT  
		Size: 15.8 KB (15799 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b435ea3ea1d1629541320fb08ffdbd6edc6d437d8ee4400ad5aeec764469cc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267065463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0472ea253c6ff290ffd7b909d98fbe14824fc6dbb40cb7c7ab3f7a137e7ef713`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:45:11 GMT
ADD file:8a1de5e2eb0c974503a07ee47335076f6fd201d377d647cbc5454453b71f05dc in / 
# Wed, 14 Feb 2024 01:45:12 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f12fd75c9aeabed692ef7b5d8a691db1e8f77911ac84bdaba43458300ab36fb9`  
		Last Modified: Wed, 14 Feb 2024 01:47:06 GMT  
		Size: 51.0 MB (50996218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f5782b608cb55c41f80fe5c4e8c6606f42add68733d4172117af3cbf2d90aa`  
		Last Modified: Wed, 14 Feb 2024 11:17:14 GMT  
		Size: 15.2 MB (15244449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a003c748b403d0a5b2399789b7b6cdf9949682c766e43a151839783904dbca`  
		Last Modified: Sun, 18 Feb 2024 05:21:53 GMT  
		Size: 200.8 MB (200824796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:07dd5269a2946c9d98412754fe76318ae6c4a587b09e5fbced1aec18f18efee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4441497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d27c525987df4b8b0a0ae8b77e6fa539d66d267c1b5a0e074af552351f40836`

```dockerfile
```

-	Layers:
	-	`sha256:f96c4ead20a5d489adda8c8e43fc45c1813044ee8f7a5c5243371a9d4030ee3c`  
		Last Modified: Sun, 18 Feb 2024 05:21:48 GMT  
		Size: 4.4 MB (4425856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be090820b9bd8adbc961c1e1976a5887b923a8dfea08503dbf8a7009d0c73d39`  
		Last Modified: Sun, 18 Feb 2024 05:21:48 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json
