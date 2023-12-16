## `openjdk:23-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:115109c57cbd6edde324dd92ffd147ec5eaa958c47a3d5972ba8cbe1a700928e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:ad20eb1e3571e87dbcbba029992e3efb25da5806156286d37ea1115ba18d7225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267685961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20633cb0fbd071344699bb1f82b4bd47e04eceeb772bf09d1dd86f544d7bcd23`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 14 Dec 2023 23:21:44 GMT
ADD file:74b33794f8e61e810f09c38da020f9becc9f6987d22fa6f42af6b4226505e6ca in / 
# Thu, 14 Dec 2023 23:21:45 GMT
CMD ["/bin/bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20e4dcae4c693910efbf28a556e2fa88ef717e15364f63da7e0a4a130b9b714e`  
		Last Modified: Thu, 14 Dec 2023 23:23:14 GMT  
		Size: 50.5 MB (50499235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d728eca023c672f716b0b6cd6f7341381f82c8e5ae816999744c820e41c3243`  
		Last Modified: Sat, 16 Dec 2023 01:51:57 GMT  
		Size: 14.2 MB (14232162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4cd8b3a81a429f174bea8e51183b04417a09227cbd1e6c0e3d7d51b3b735e3`  
		Last Modified: Sat, 16 Dec 2023 01:52:06 GMT  
		Size: 203.0 MB (202954564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:d5e92733d0c82020d1a4722bee4d42aec757e8fed6e28fe08030efb8985b2378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73081b8a180ca09b90eb1f7eb34c5da3cd97531a9c1eeeb94ac174ff7c6dc5d`

```dockerfile
```

-	Layers:
	-	`sha256:16577a19740be86bd144c7f6b31f1c9c2b0ed50a2f00929cf550d37e9363a540`  
		Last Modified: Sat, 16 Dec 2023 01:51:57 GMT  
		Size: 3.8 MB (3768680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a458ba935b2945d5cd338e82152ed8c3e562e8ca098f235c7894851fd41be122`  
		Last Modified: Sat, 16 Dec 2023 01:51:57 GMT  
		Size: 16.4 KB (16386 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9caf5f9fef66e1a8098d643a7747cc2973b0d301196b2dd54f61ec5afca052d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267214429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbffb7949d403e19fc2d8f7b06b5ee302ef7673177a3b3e969cc6bd9c55632c7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Dec 2023 00:02:56 GMT
ADD file:7f9b20722f4f2c781b7814e113711ee10ee458be84fe343e7d61658ede9c4711 in / 
# Fri, 15 Dec 2023 00:02:57 GMT
CMD ["/bin/bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
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
	-	`sha256:c3b9fe90dc5357495df5705f07846bd144773fa37d428d6493a81ed27599c154`  
		Last Modified: Sat, 16 Dec 2023 09:40:14 GMT  
		Size: 200.9 MB (200861754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:8dcd9208db04c38a923f3903206032bfb3a66b0f66bd511743809617c6cf1b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e90cf0b4a0f618b1f1269f833ad74668ddbe26dc57a9bd2b611aab70ecab704`

```dockerfile
```

-	Layers:
	-	`sha256:d67ab5c70ec09c198637c336da3b2e2deef1c8df5ae68f3678b30a0627a185e8`  
		Last Modified: Sat, 16 Dec 2023 09:40:04 GMT  
		Size: 3.8 MB (3764553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:483b7f19f8d7ca744911cd0f07a76ab85baf650e6c759c61f7ea19eda6910dbb`  
		Last Modified: Sat, 16 Dec 2023 09:40:03 GMT  
		Size: 16.2 KB (16233 bytes)  
		MIME: application/vnd.in-toto+json
