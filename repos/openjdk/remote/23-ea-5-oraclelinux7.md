## `openjdk:23-ea-5-oraclelinux7`

```console
$ docker pull openjdk@sha256:44008c7ae183ec938809869708fcb23be247ec8afccfe2ddc886c3d96fcec41b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-5-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:c4d86f43ac925369d5ce93fe290ab7320142f87080b8ccb8c1cc0f930ff0994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267681139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f1e6f36dbcb7196df4acc500ae8c401853b825aa9a42450772cbd242027d02`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 02:00:35 GMT
ADD file:bbd183ec68733730893e5ca4bc8673cc42d54ecec8fc30444474122a66c84dab in / 
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5dd0ec2f99109a7ed9268ac1405fb9951743210620437ec13df10714ebe89b00`  
		Last Modified: Wed, 17 Jan 2024 21:37:41 GMT  
		Size: 50.4 MB (50385815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63d9b61173bb2ca333e0b98439c0f17da853e1b9319a9b67d0d153f054784c5`  
		Last Modified: Wed, 17 Jan 2024 22:44:08 GMT  
		Size: 14.2 MB (14232292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4885f2e7a58745f539bdb3e47868a0f70aeadad236b403e1451dbbef9de6a986`  
		Last Modified: Wed, 17 Jan 2024 22:44:15 GMT  
		Size: 203.1 MB (203063032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-5-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:1b76e863afbeb26b6148dd66b9ff50f3b4f6eddf4cebce52a6817b325cb72d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09b4aea881942c0373f333b4507213193150cf3432381663d4ee54e484e8953`

```dockerfile
```

-	Layers:
	-	`sha256:0cc2e6a2e346f7d665f067edd52d9f7369dd7ca3d060f0670611f8655b63b254`  
		Last Modified: Wed, 17 Jan 2024 22:44:08 GMT  
		Size: 3.8 MB (3768682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e59048a7e5197f2e1d11efd290356ad0779f243b5b50f4641065796f8a91655`  
		Last Modified: Wed, 17 Jan 2024 22:44:07 GMT  
		Size: 16.4 KB (16386 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-5-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8d5455e3008c9adc664faf5579d99dec9713aae09be61ebd331342a936039e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267325117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b1b9e98fe4338172c5e10aae432f937665be00be46784788636156b0c6a5b6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Dec 2023 00:02:56 GMT
ADD file:7f9b20722f4f2c781b7814e113711ee10ee458be84fe343e7d61658ede9c4711 in / 
# Fri, 15 Dec 2023 00:02:57 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
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
	-	`sha256:b9219abce42d5b31468280db64ee149eab6e5509246a073b00a7701d96e49159`  
		Last Modified: Sat, 13 Jan 2024 01:38:44 GMT  
		Size: 201.0 MB (200972442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-5-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:b30f5694fec08dca057af83dce0620e8d7c2ece4823233ff9126ecdab8e901bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80da042b170b457dbceb58fc53864bbd2d7ebac71fe40b7aaed8f278c0af6c41`

```dockerfile
```

-	Layers:
	-	`sha256:689f9b97c398802abcc3b3dc211a9e0174675b5a1eb33e80936a89143acb8308`  
		Last Modified: Sat, 13 Jan 2024 01:38:40 GMT  
		Size: 3.8 MB (3764553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18475137c78840bb03ce943f09ea4579ea1baa6bbcbb8d74197b6390f4455341`  
		Last Modified: Sat, 13 Jan 2024 01:38:39 GMT  
		Size: 16.2 KB (16233 bytes)  
		MIME: application/vnd.in-toto+json
