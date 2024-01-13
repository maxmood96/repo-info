## `openjdk:22-ea-31-oraclelinux7`

```console
$ docker pull openjdk@sha256:130f4e9c7f8b449fcfd1d00ff2e3ed9a322af16b7693894198e014c805b24a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-31-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:6d9fee93b2ff2f94df772a544e480ee10cd1d1283dc001cf192b7c9b803b751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267487390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a23cf8589f015ed640dcbac3a11ecd8dc2be55b5c12c2f9fe9149de35348f9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 14 Dec 2023 23:21:44 GMT
ADD file:74b33794f8e61e810f09c38da020f9becc9f6987d22fa6f42af6b4226505e6ca in / 
# Thu, 14 Dec 2023 23:21:45 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20e4dcae4c693910efbf28a556e2fa88ef717e15364f63da7e0a4a130b9b714e`  
		Last Modified: Thu, 14 Dec 2023 23:23:14 GMT  
		Size: 50.5 MB (50499235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5340e4878403ed97ab5bdac65e9dd104a2e1dd239de197852dbce80f4db3650c`  
		Last Modified: Sat, 13 Jan 2024 01:07:43 GMT  
		Size: 14.2 MB (14232200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0ac6fe66ad832e08b5e92b7fe0b685e8441c6e69ef68f8faa4e5a5da03a1b1`  
		Last Modified: Sat, 13 Jan 2024 01:07:47 GMT  
		Size: 202.8 MB (202755955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-31-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:0fc4c13b1c71d0d138c18c85a6325eee572e85a2833aa478f07655fa104a4470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ac5f2fb9ab45b400bca931c0ad41cc791c9b0f1cacec142c5870a4ac960f2f`

```dockerfile
```

-	Layers:
	-	`sha256:006f9459ecb998ca0fb46b39979e6297c13183817567eaa6268c1346ee182d1b`  
		Last Modified: Sat, 13 Jan 2024 01:07:42 GMT  
		Size: 3.8 MB (3768690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81bd11f3332687fc25cf7579ec705dabd06a27f7cd14b26cb4434d5a7a9990a6`  
		Last Modified: Sat, 13 Jan 2024 01:07:42 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-31-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e33f1fd67dc7d95fe2a1e6814db657c9ea4f842752439225874d7244069ecb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267169198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589df2023826c49c0d1e5d4c3eeb55291b284070c4654e9276ce5c30210f9f55`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Dec 2023 00:02:56 GMT
ADD file:7f9b20722f4f2c781b7814e113711ee10ee458be84fe343e7d61658ede9c4711 in / 
# Fri, 15 Dec 2023 00:02:57 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01eab324a7fc4cacc34c78d38ce9548750df098b20899d269b500307b6765a1d`  
		Last Modified: Fri, 15 Dec 2023 00:04:16 GMT  
		Size: 51.1 MB (51110815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96633a794a03133d53bf43854186ba59a38c777f78fe1e7226aff149ef8d228`  
		Last Modified: Fri, 15 Dec 2023 23:21:22 GMT  
		Size: 15.2 MB (15241860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a60dc03394fcab1779ed6296cf6187bac975b51e4f364ea3b7900b7a886a0`  
		Last Modified: Sat, 13 Jan 2024 01:44:11 GMT  
		Size: 200.8 MB (200816523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-31-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:cf591ff864c1d23914d62cea248f6fd4ad82bd10be4a7387a8dbc4cb3de21c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684501966ec35022917294e6e5f8f0888ee576193ff7fe0cf7e873c596f1fb9e`

```dockerfile
```

-	Layers:
	-	`sha256:e5ba5f6135a662bd5a4a9030613642723b16e11295281792dbdfa029ed4a687e`  
		Last Modified: Sat, 13 Jan 2024 01:44:05 GMT  
		Size: 3.8 MB (3764557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7657bb9811e719dd3ee8e5fe5214b63fa1bff82c44c91661208df6afa17f76`  
		Last Modified: Sat, 13 Jan 2024 01:44:05 GMT  
		Size: 16.2 KB (16250 bytes)  
		MIME: application/vnd.in-toto+json
