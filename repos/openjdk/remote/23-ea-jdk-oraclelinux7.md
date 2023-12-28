## `openjdk:23-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:0615b29c8435a2cead4b6e7ac9aa0f2cceea333eb2eb7668ed253eb88b16e6f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:4cc0948f3547a848b879b5104b2de3db6c013ef9f62ce38d169f04bffdb0dc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267722334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74e12539969a59c438ad1424fb8fe5866c62d6c8d789aae475fdc436660d315`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 14 Dec 2023 23:21:44 GMT
ADD file:74b33794f8e61e810f09c38da020f9becc9f6987d22fa6f42af6b4226505e6ca in / 
# Thu, 14 Dec 2023 23:21:45 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20e4dcae4c693910efbf28a556e2fa88ef717e15364f63da7e0a4a130b9b714e`  
		Last Modified: Thu, 14 Dec 2023 23:23:14 GMT  
		Size: 50.5 MB (50499235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f576ebf92acca67f3691cd5e8ba4665efbd3d7bb5f10aae2d4db7ee1dc27c823`  
		Last Modified: Wed, 27 Dec 2023 21:54:13 GMT  
		Size: 14.2 MB (14232194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93915e549f0702613de1c93d4ff173fb5e57446d1ba238a9a43e0cfb69946558`  
		Last Modified: Wed, 27 Dec 2023 21:54:16 GMT  
		Size: 203.0 MB (202990905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:0ed11dfca14d71314b687833380dfb8467a2403891d992ee55e7a99d1eb3a323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151a823e5db731bfed8ed24db2014e6dcd44a92ade20718aab64df59d9bba577`

```dockerfile
```

-	Layers:
	-	`sha256:4bc5c206a601998d81df8fc7e71ff8d6e62bd72bff36ad518520c4e94db5e207`  
		Last Modified: Wed, 27 Dec 2023 21:54:13 GMT  
		Size: 3.8 MB (3768682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e1241e9d9d45c667e77ec73566b50836675df371f67b315133a22586e2e384`  
		Last Modified: Wed, 27 Dec 2023 21:54:13 GMT  
		Size: 16.4 KB (16386 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:23c3de90e831682af6b21ab46c8a6f7c7aa2d1ce23dcbb187171a177f8f26bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267245175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8aa485c39e3f512101e662ccc67750a3a4635bc35047880db98fbeb1347e69`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Dec 2023 00:02:56 GMT
ADD file:7f9b20722f4f2c781b7814e113711ee10ee458be84fe343e7d61658ede9c4711 in / 
# Fri, 15 Dec 2023 00:02:57 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
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
	-	`sha256:299a79c4bf13241dced9b9053a58d7b4fa01f342336950cdcfd15c1b42cd50af`  
		Last Modified: Thu, 28 Dec 2023 04:49:19 GMT  
		Size: 200.9 MB (200892500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:a02d11de483a4bdbea64fddc5e7f804d8b55dae65f0099b9a89f029a9724b587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc02bf188817a192951334675e59e3902584f2c8b1ab96ffa3f5ece50bc3509`

```dockerfile
```

-	Layers:
	-	`sha256:0246a0364cd5b7349391518f39388899d4e812bc29f1c83230e7279565adebb5`  
		Last Modified: Thu, 28 Dec 2023 04:49:15 GMT  
		Size: 3.8 MB (3764553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a4b59526bbb6fdb0a68349f81fab7bf145532e689459ddcf62b2b628e99135`  
		Last Modified: Thu, 28 Dec 2023 04:49:15 GMT  
		Size: 16.2 KB (16232 bytes)  
		MIME: application/vnd.in-toto+json
