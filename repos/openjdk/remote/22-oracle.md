## `openjdk:22-oracle`

```console
$ docker pull openjdk@sha256:bd48559bcdc0528731e1d31b5c4166d5b743237f0c2dd51d365f09126b09828c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:2233d278c8b49c8b7de5282466fea30ddcb4939debaf3432ca40c7465f3b4c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269068512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e33e09c8d3eecb1a5e979550eec5ce86e997c96e5a66979bacdea9e7c513f50`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 01:48:33 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723af731e9e371bafd214069b5a120140241a0bb3e15e46d0f27df5a2a10b85`  
		Last Modified: Wed, 17 Jan 2024 22:44:18 GMT  
		Size: 15.0 MB (14990843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594bc9647a66fd2295bd5189a488b0c762b663f5ce514210ef7f7964c69faec8`  
		Last Modified: Wed, 17 Jan 2024 22:44:23 GMT  
		Size: 202.8 MB (202755938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5bc6e01126806fd761c2bfbdd58b60cc8509e468a9b297fbb1deb93b1e0e332d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452fc6d21949af8cd73abdca5df2bf20e0327cc353e8c9690b2a13fcd3c56e7c`

```dockerfile
```

-	Layers:
	-	`sha256:5389cd9377fb7dcf8de6777481e3f2d8ee47fe9e9a0cb2b60ee0705b72f9f47a`  
		Last Modified: Wed, 17 Jan 2024 22:44:18 GMT  
		Size: 1.9 MB (1915859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51bda4f7e160b892ec5682d9c2a013c74771c37d911534f11966e25141d9d58`  
		Last Modified: Wed, 17 Jan 2024 22:44:18 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4114998ccba14935a706c925b6267c7d3d12098f0c9d161129ea332ee96c198a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266593385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55f13477f769fdb32de3e1ca4e5460637d44cc07324fccd97f594686cbbf706`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 01:48:33 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbecf34c8e1a9b9949041e4c9e805d7ee8c1f00ad6362349a4579d6db495c27`  
		Last Modified: Thu, 18 Jan 2024 10:42:33 GMT  
		Size: 15.7 MB (15702213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39771e196bf8284fc24126bc46b73f5f346eca1159f7c4d7904d0026aa830392`  
		Last Modified: Thu, 18 Jan 2024 10:44:45 GMT  
		Size: 200.8 MB (200816594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3688b2de8c050aa75dd2006788a6827f9983dd904e7d7613c0dcbd473ab4eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c84cb9017c384b6ff9f8f4bae45fa7aab04799f52f14c85ec5d6bc0ae7bd337`

```dockerfile
```

-	Layers:
	-	`sha256:731e295fd3ba8d47f33d3c974e92651ab3a862b7ac1445c4e3200ab61c384d98`  
		Last Modified: Thu, 18 Jan 2024 10:44:39 GMT  
		Size: 1.9 MB (1914433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b471e6f0d35d87035bf67ebdc349df0dba11beb0a8ca13ce312dc55a1e065e9b`  
		Last Modified: Thu, 18 Jan 2024 10:44:39 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
