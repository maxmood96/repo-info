## `openjdk:26-ea-21-oraclelinux9`

```console
$ docker pull openjdk@sha256:8323b407217e546f866961c250e846e73ab8a29f7d28fed05fc7a763de0fb8d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-21-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:0a517f270ff39256404e871730a93fa0e86e38fb8298e56be1c9f67a469e6a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313311548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadd932ee2bc7a71f7662cc33496c8519c336582d3379bbaa105c8a80e07dfb6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 24 Oct 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Oct 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='3189ce7f96b6fb0b69ce1e8ca7bc626aa30009023f9e2ddf7faeaa5ddf9e8626'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f2d4dc408e6fe82574fb9ad9cff97da63a897a887198c666cb1bd0987fa690c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8d658d69293c03c91247e6c1996b630ebc66904114948775ca71904f5d39a`  
		Last Modified: Fri, 24 Oct 2025 23:21:25 GMT  
		Size: 38.1 MB (38087542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ff58ddb89c9b6883dfba586c768538dcf1acd1da205e565f91282d148c874e`  
		Last Modified: Fri, 24 Oct 2025 23:22:53 GMT  
		Size: 225.7 MB (225727501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-21-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:b70cf21a902fd6eb0de6b3f1d2ca542694f919ad755b4bd60a119b30b99dc2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe7698cd3e4afdf9f78ec99a5e77cc818a6dc03e379e7efc5bea9f898589c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1a4c8192382a5e3ba9f3f1153de2c175df3b4f10515e08cbf2ec2b8e086072e3`  
		Last Modified: Sat, 25 Oct 2025 00:23:25 GMT  
		Size: 3.6 MB (3639498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fbbceceb73945e590ef1880a167ffbd501d46d52790051c2ab49dd5fb9564e5`  
		Last Modified: Sat, 25 Oct 2025 00:23:26 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-21-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:53e929fd7117cd5f9472d0a7464798a87a2624b3b1bfba53b017e5e34b245610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310159751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d2452913f30d6f6a916e7d499daa41056ed77884651d1714cb0a1faac9bcab`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 24 Oct 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Oct 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='3189ce7f96b6fb0b69ce1e8ca7bc626aa30009023f9e2ddf7faeaa5ddf9e8626'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f2d4dc408e6fe82574fb9ad9cff97da63a897a887198c666cb1bd0987fa690c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea87f104f650863198109ef81db30a3fadf317510cf11259a738132b047ce218`  
		Last Modified: Fri, 24 Oct 2025 23:24:03 GMT  
		Size: 38.5 MB (38491436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53d4640b44d6c7bec0213245d472b5b5600fbdf171f75afffa27df8e384e875`  
		Last Modified: Sat, 25 Oct 2025 00:40:48 GMT  
		Size: 223.6 MB (223581414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-21-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:7f77ed86314c00723be9ab742eafbb26db211964618179835cf7c85cddf5575a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3657292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb88322ec204487b9186d53828499a0812d1eff4cb55f7b65572f470c7bc178f`

```dockerfile
```

-	Layers:
	-	`sha256:c2690f689c26ec734ef2bc0c020508b70b4a181f2a7478b778aed2f0a7ddacaf`  
		Last Modified: Sat, 25 Oct 2025 00:23:30 GMT  
		Size: 3.6 MB (3637260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a3488fa1fb34b11a1968823be74ef62a79a775f8b1bec6ab2bbc726eac4d9c9`  
		Last Modified: Sat, 25 Oct 2025 00:23:31 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.in-toto+json
