## `openjdk:23-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:bcab526d8623463b598a7783888cf4243eeedd0f3373ecab9ef5811ca4730f60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:cd87f1d62c67b60097c4838fe0a9eb4b91c93786b812d4e0c272c07b2de40267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297551621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cec48b63d4a98c9f9c30841fd3bb50080a8944728f616a11fad86f00f4a6ca`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 29 Mar 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+16
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='9a5d2039ec965c15d80dbc5106c9e2f1c4a80975e18d308b55f0a3d892f24358'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d654c940f0c5b9ed7549f29066599b2caedbaf2ec45f3745ac35e265c288e2d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbf4f4dc71ce7e8d9dedecfce938d38a4b26b1110c663ee2812d0704ccb5ad4`  
		Last Modified: Mon, 01 Apr 2024 23:50:22 GMT  
		Size: 37.7 MB (37737870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624c43f938edff95cb6097024ee9ff260fea7ac8fbdfa92ee7ca59814832643c`  
		Last Modified: Mon, 01 Apr 2024 23:50:44 GMT  
		Size: 210.8 MB (210835297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:01fc4a3cc076c9152778d3ec0a0503c1ce88eb78c30406cea86334b1bc233cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee6c8d58c25c0c514025c4c0acfe0e7b5eed05aacff50a9f9cde51ce03608c1`

```dockerfile
```

-	Layers:
	-	`sha256:c4fad1e8d0bacbfc6c0908f368978769b22d18d7b7919fb5df770cd253081482`  
		Last Modified: Mon, 01 Apr 2024 23:50:22 GMT  
		Size: 3.3 MB (3329538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec16595f4f4f8d9f58d03fa004f24331866d12a3a5afdd122bae3fc8ad1c2781`  
		Last Modified: Mon, 01 Apr 2024 23:50:21 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:85cee66eda14236904605fab974035c76321299d6782897ed33ebd0b8d41eacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294536931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba84b054795c06944f77535018f4cbe547c0420e4373f6fdd6cef4a0f54cf555`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:48:53 GMT
ADD file:71724b501850c3e6cd72efc58b3430394f691a428c2c62755eac0b93c5579f35 in / 
# Fri, 08 Mar 2024 19:48:53 GMT
CMD ["/bin/bash"]
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 29 Mar 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+16
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='9a5d2039ec965c15d80dbc5106c9e2f1c4a80975e18d308b55f0a3d892f24358'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d654c940f0c5b9ed7549f29066599b2caedbaf2ec45f3745ac35e265c288e2d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c53b3bc8702e4b172b3fdde99731082a493b5f5fdd7e9632b3cf7dea02a52b4`  
		Last Modified: Fri, 08 Mar 2024 19:49:57 GMT  
		Size: 47.7 MB (47664888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71597242e3bc84850918d978b72bcf84c5867bfb6441051c67b805dca13e66a`  
		Last Modified: Sat, 16 Mar 2024 15:50:44 GMT  
		Size: 38.1 MB (38140694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a614182f9de986fbfd9886426bb38a387cdc08ba19211114f9a1288d0fc5670`  
		Last Modified: Tue, 02 Apr 2024 00:07:37 GMT  
		Size: 208.7 MB (208731349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:27f65e34c796381f05392be02a412167a655b85046fe7b318fe9b2952b9d2c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab42e68c647aaa103d891760d4fe5ca0f594708278f925b96b8aac1b4689c4ce`

```dockerfile
```

-	Layers:
	-	`sha256:2a6711d015f0aca57083720590781ebab01a75cc980f3839fe7e286bc4d53d0b`  
		Last Modified: Tue, 02 Apr 2024 00:07:32 GMT  
		Size: 3.3 MB (3326760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab93b58c606f23e34e0cab7e922d43a6e64eae57a0c0696a193033d5c470869f`  
		Last Modified: Tue, 02 Apr 2024 00:07:31 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
