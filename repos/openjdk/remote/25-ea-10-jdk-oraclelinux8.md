## `openjdk:25-ea-10-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:79420fd2a1e41c7c650da63135df3fc62a3cfd1b4bd598b1d1fe672838e9cea9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-10-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d47c42982efb975a21f41e7c71dfa7a60fd8d30ac85df9608d7cb58a9eeb4a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278573692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabd5c0c30b0f8ba74697ca4cf4f84aa153900591c773ce821fd2defddabb8d4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Feb 2025 23:06:48 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 13 Feb 2025 23:06:48 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:50bd714b8e38d1a822db5498f9fe090cf204274713557d5f5437e40188ac4303`  
		Last Modified: Fri, 14 Feb 2025 01:27:41 GMT  
		Size: 51.3 MB (51283059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90afa01d61cfce88687b4fbc11def579255ccfe2c1c0a1c23d0f1eff6c44a74c`  
		Last Modified: Sat, 15 Feb 2025 01:52:15 GMT  
		Size: 15.0 MB (14979091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b71bd9f08ed2b1ee8010025df2942ba2f6735d6b85e69db1768f1ac530e17d4`  
		Last Modified: Sat, 15 Feb 2025 01:52:21 GMT  
		Size: 212.3 MB (212311542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-10-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d1b38c306ed8fd1dd1fc4ec1013ca9188a5e764ddbf1553584b3f0a7e0e38089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c2524d8ab1ea8f304169929b2b4ed43c5fdea154e59dfdb2f7e9ad4b6b8aca`

```dockerfile
```

-	Layers:
	-	`sha256:90a973b1c09402ff3ad331265bb86bfb86d365195097137c3903df54d0e1539e`  
		Last Modified: Sat, 15 Feb 2025 01:24:27 GMT  
		Size: 2.4 MB (2444723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9ae681397a98ee85f0e25c0f82af0e5bc9756be6579c79c5bc607980caea4f`  
		Last Modified: Sat, 15 Feb 2025 01:24:27 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-10-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b15aa9806ea6c722f65d0f2831fb9cbc72c55797ee8163999002cb0cb7ff58fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275933522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f34630e3e66f789e9c4fc2102ceed36df59c544b5c6ea48d06b123c239a7aa`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Feb 2025 23:07:39 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 13 Feb 2025 23:07:39 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e8ec99a1e85147c24be8e8ee35b17a7fa5f9a2c30701932a58ae62802e80c54`  
		Last Modified: Fri, 14 Feb 2025 04:52:34 GMT  
		Size: 50.0 MB (49989289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d2291ce00cd6bc0d3bd9e3183640619c1993d713063dbe8f6430762533fbdb`  
		Last Modified: Fri, 14 Feb 2025 08:46:15 GMT  
		Size: 15.7 MB (15675007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3330a6cb82be844732005b496704e054517ee2ca46d2fcd64f94de8d3344501d`  
		Last Modified: Sat, 15 Feb 2025 08:50:04 GMT  
		Size: 210.3 MB (210269226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-10-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ac619be72151f543ba4f6d538938d6ef6c66d91815f35ea9e03485a5565ab9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcf5f4dea25c803c4cff44eefed513101a03f635eb69c5d04628bf5e665e9c7`

```dockerfile
```

-	Layers:
	-	`sha256:c26ea087fade8196519464a1599d4a983948adf0b96644a35eae6b341e33cf36`  
		Last Modified: Sat, 15 Feb 2025 10:23:59 GMT  
		Size: 2.4 MB (2443569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee32f54f7c9927807fbf71583d21e6fc7ef288ca2986155ee80fe7876f0a450`  
		Last Modified: Sat, 15 Feb 2025 10:23:59 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
