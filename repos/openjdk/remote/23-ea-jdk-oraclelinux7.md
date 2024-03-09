## `openjdk:23-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:5d114cb415868c762e629a1506c79165fedbe5ce692665ae6230c4c657a60380
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:5ec3c17e77727a81891c8bcb6445a8c9b8e12ca24ca8535cddf51142ddd9d1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267435129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362bb910030643d934e3aa3a303db3b5d265591a393c2ba237e39d998a25225`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:52 GMT
ADD file:6c43f1bc1b598f7b1a5fc6f5c7951e8525eee01704f8f5e5caec8a944a4ecb4d in / 
# Wed, 14 Feb 2024 01:47:52 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ff90099b5a4df32952d1822d472a72c931c53a68c05a3ba7431ea0f85d54135`  
		Last Modified: Wed, 14 Feb 2024 01:50:04 GMT  
		Size: 50.4 MB (50389833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf494753a54e7c5e6b9cc1004f018ffb1c34fa3361b5116c20f3e743b691343`  
		Last Modified: Sat, 09 Mar 2024 01:49:13 GMT  
		Size: 14.2 MB (14231474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da66f0d69bf846d8cd83a11a1f50540f4557473b653297d167fa37c4efe41dcc`  
		Last Modified: Sat, 09 Mar 2024 01:49:15 GMT  
		Size: 202.8 MB (202813822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:92354badc31176e7be25f184539741b396e0072627bc62afaad757e118b12266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384e4a7981f0815b48c4a8e0649077e94e2b781f2b3b255a26be80c5f92630d1`

```dockerfile
```

-	Layers:
	-	`sha256:5547932e7b50ac90352bd9d606fc7d8dfc4aa1bf2179b489d5c65e41267dfdb1`  
		Last Modified: Sat, 09 Mar 2024 01:49:13 GMT  
		Size: 4.4 MB (4429923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d24822ad9cf1427817ab4a18a186a364d13d4137b12ab84186dc8fdb847aa00c`  
		Last Modified: Sat, 09 Mar 2024 01:49:13 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:81563dc1999e5ca2fd4a8224638323343c74f99b225b3ea193198d47c663e1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266920086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82fd222433fd8da09b5afb53a4e2583b1dc483d073269909e4739baa7c20f3a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:45:11 GMT
ADD file:8a1de5e2eb0c974503a07ee47335076f6fd201d377d647cbc5454453b71f05dc in / 
# Wed, 14 Feb 2024 01:45:12 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f12fd75c9aeabed692ef7b5d8a691db1e8f77911ac84bdaba43458300ab36fb9`  
		Last Modified: Wed, 14 Feb 2024 01:47:06 GMT  
		Size: 51.0 MB (50996218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf9cd78eb79707088f78d22efbb6aa4e6bfacee4404ae12f36d9e2168c53f18`  
		Last Modified: Sat, 09 Mar 2024 03:57:21 GMT  
		Size: 15.2 MB (15244613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1640eafc9a99672217eaae8a7b54df3191989ceced79e102040a4f821d4f89`  
		Last Modified: Sat, 09 Mar 2024 03:57:25 GMT  
		Size: 200.7 MB (200679255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:8d659b6d3cb70b1ff0eabc54f63ad0ac726379ef1587c1f1d130c0d9c30d0318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4441997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b01a16b50ef81f5ef4cf31c0c3f6e9c7a84077f70f6a007b6fb94d9d1135066`

```dockerfile
```

-	Layers:
	-	`sha256:7df08463f98b05f821651d88da0466f8138afd55d5b10a15fd1d320f59d0aeac`  
		Last Modified: Sat, 09 Mar 2024 03:57:21 GMT  
		Size: 4.4 MB (4425580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8518ce1f10762b2321e36976124a42549d5532918bd122c28f83c0f962400348`  
		Last Modified: Sat, 09 Mar 2024 03:57:21 GMT  
		Size: 16.4 KB (16417 bytes)  
		MIME: application/vnd.in-toto+json
