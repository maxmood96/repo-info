## `openjdk:23-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:df7818d3cb36f7bfa3eb3f55dc60672c3283b4e27da72631cd5219adaf7a1d63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux7` - linux; amd64

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

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

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

### `openjdk:23-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:967c6df11ed5f89889da6749055595fc4a33c8bf75aa91521dee48a44896de42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267230700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e8873fe9be2bf82b7e90c756afe314d204a163ae36d41465f26de8b9b19af6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 02:00:35 GMT
ADD file:8e4f54dbc6703a8208e63085c4e5598de223be1f27406807e223bc6ef121c4cf in / 
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
	-	`sha256:963289c7c202b6b90d04fa4c851434fe886f6eaf9d3f3cd608dd53d3616791ea`  
		Last Modified: Wed, 17 Jan 2024 22:10:14 GMT  
		Size: 51.0 MB (51000317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385c41166173f9457fc478a9d47f500342a45b6725b38dbcfe193311857a8963`  
		Last Modified: Thu, 18 Jan 2024 10:43:55 GMT  
		Size: 15.3 MB (15257951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681145cf7e15397660a40847e031d19fa1ff8166f3e774027ef1fc7d44d98f5c`  
		Last Modified: Thu, 18 Jan 2024 10:43:59 GMT  
		Size: 201.0 MB (200972432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:6ad43055a872d4f04a8d0ea68ea8ac11875872a5f468fa18094e3f4800322f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1139e431f58c82c79e70cda5a7a254a1b8df557bcc363e7a0281aabdca3ef96`

```dockerfile
```

-	Layers:
	-	`sha256:f16ab7d50d2973b58a75b9dea4e49ac221a181dadc4376c5524c1726d37dc909`  
		Last Modified: Thu, 18 Jan 2024 10:43:55 GMT  
		Size: 3.8 MB (3764553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91ad6a8ea5dc83ef5e5d2cff04a765d466f802849734fbb74a1956c916b2f43e`  
		Last Modified: Thu, 18 Jan 2024 10:43:54 GMT  
		Size: 16.4 KB (16399 bytes)  
		MIME: application/vnd.in-toto+json
