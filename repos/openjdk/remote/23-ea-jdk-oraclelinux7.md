## `openjdk:23-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:68a83327a5298acc15a9a89b6980ce6e02bf730f26a5d8c3ec2844e4767a20da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:f72c2931309d037eb36ce7661b2d6816b8176af26a0c3868d95068aac2170460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267757917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3aab039a7c4be15237ba69603d5b617ae8556c0c9c3d588696513b285204aca`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:35:22 GMT
ADD file:bbd183ec68733730893e5ca4bc8673cc42d54ecec8fc30444474122a66c84dab in / 
# Wed, 17 Jan 2024 21:35:22 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5dd0ec2f99109a7ed9268ac1405fb9951743210620437ec13df10714ebe89b00`  
		Last Modified: Wed, 17 Jan 2024 21:37:41 GMT  
		Size: 50.4 MB (50385815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e235dcef8b11bd0f2d310add16567b958030ec619e2a767a7fc17a0d2c487b14`  
		Last Modified: Fri, 02 Feb 2024 22:53:43 GMT  
		Size: 14.2 MB (14232314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5966ef835b765ba23f241e247adae878373870a344ad2505a2d5dbb16e61c83d`  
		Last Modified: Fri, 02 Feb 2024 22:53:45 GMT  
		Size: 203.1 MB (203139788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:b64ea9fe797800d498dd959485a6120500d7d6e49a945db910f31c8bd84e4db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77010d3efb3cb649e1740c048225b6e5c5c8687c504852389be35e066fadac7f`

```dockerfile
```

-	Layers:
	-	`sha256:487fe90859893b32505c9f56e9f076394f638b91e78b6f295ac8f66443ae559f`  
		Last Modified: Fri, 02 Feb 2024 22:53:42 GMT  
		Size: 3.8 MB (3768689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05612fd6d193ff85cd386cb6ef32d5f94b126127991674f64bf6216b831a2325`  
		Last Modified: Fri, 02 Feb 2024 22:53:42 GMT  
		Size: 16.4 KB (16386 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:602bfb564cee416f5e2f8059af95d7bc15e5992f57c74f43f8440374fd24e7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267274793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527330bce4292ed5b5def067141c64b0c813777ad92790e3681793a125b01216`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:08:17 GMT
ADD file:8e4f54dbc6703a8208e63085c4e5598de223be1f27406807e223bc6ef121c4cf in / 
# Wed, 17 Jan 2024 22:08:18 GMT
CMD ["/bin/bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:963289c7c202b6b90d04fa4c851434fe886f6eaf9d3f3cd608dd53d3616791ea`  
		Last Modified: Wed, 17 Jan 2024 22:10:14 GMT  
		Size: 51.0 MB (51000317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42a06ab66b43a901c035f28bcf7a5d44201a1d0f6130c5d26dcce4d2d409c86`  
		Last Modified: Sat, 27 Jan 2024 20:34:04 GMT  
		Size: 15.3 MB (15258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad02ad1f1afd36a34694600eccd09ee36b9ee4b02613263302cd058ed250d6e`  
		Last Modified: Sat, 27 Jan 2024 20:34:08 GMT  
		Size: 201.0 MB (201016457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:409bc544eef663ced2e3758309e251901b05150810f33835765bb5288296d2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1f6d6b7a28e0d45df5cb78703bc2fef8e475027798e1ed3bfa250e1d62eea1`

```dockerfile
```

-	Layers:
	-	`sha256:283843cf04fe9c8b1df455786824b83ffe762beb76e7c7b5798bddc2d321abcb`  
		Last Modified: Sat, 27 Jan 2024 20:34:03 GMT  
		Size: 3.8 MB (3764553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccbbb31ec2df9fdab580299d743b150d309f74b6c5fd96140a9a3b9cd49acb1a`  
		Last Modified: Sat, 27 Jan 2024 20:34:03 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json
