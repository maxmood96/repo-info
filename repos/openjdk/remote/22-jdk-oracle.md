## `openjdk:22-jdk-oracle`

```console
$ docker pull openjdk@sha256:28494e8e002026bd9d9ede4f9faa1375b016d9a5a1b13b6e453d4fda982ae194
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a838ced3d27977260fb6742fdea045835eba457ccdb33c79306abce8e3ba0ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269101260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe48dbda24530c398766b4233f5fd8f28f3740b4c72cb70a3e753008bcede55`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Feb 2024 19:48:11 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 02 Feb 2024 19:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='170b7192de3e30c796b95d765b12ca457d3f4b05e97bee0bf81709c8b43cd992'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='63460b6a2c4d547d7a8cf4cf86d67a46f5e6a96a62843a787a2aabdbed4df119'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5e909313650562f8bb3664a095307750ad6b53937d0db7d3f256ecc1726663`  
		Last Modified: Wed, 07 Feb 2024 00:50:03 GMT  
		Size: 15.0 MB (15005708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3461f9fccf6abd1a30064cda1683ec92020703b87e3496558dc787fa58114a44`  
		Last Modified: Wed, 07 Feb 2024 00:50:06 GMT  
		Size: 202.8 MB (202768161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:46cdf911cc72e2a634d26be6e21ef3157578984abab5f8a3df750b19d6e66fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874849dc0c060e4f3bcaff6e3f7a72745fc664917acf26967ad27fdfe9abc963`

```dockerfile
```

-	Layers:
	-	`sha256:4b7ff2d814331a4722ec56447570e2eac92476016973b746c55a6c251197229f`  
		Last Modified: Wed, 07 Feb 2024 00:50:03 GMT  
		Size: 1.9 MB (1915894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4beae0dbf21dac31ace572cf5481ae0f3ee42404eac5149502efe2bc7300e9c0`  
		Last Modified: Wed, 07 Feb 2024 00:50:02 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6f3636e911677edc568e842f741fa991996128ee13a96f33475438cb047ad782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266588180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d593daa9dd602d2eccf9462d3335d97f13cb0c3f6dde0c4277c97bfb31cf83b2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Feb 2024 19:48:11 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 02 Feb 2024 19:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='170b7192de3e30c796b95d765b12ca457d3f4b05e97bee0bf81709c8b43cd992'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='63460b6a2c4d547d7a8cf4cf86d67a46f5e6a96a62843a787a2aabdbed4df119'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04d3eef9c8a6237c8b46c9794501777a8ce3c58a2e3a645da53db98f8e028aa`  
		Last Modified: Tue, 06 Feb 2024 23:32:40 GMT  
		Size: 15.7 MB (15691300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f373500f05660cff87f9b699780e4eb4a0864851d2795c185ff74f51ca20ca9`  
		Last Modified: Tue, 06 Feb 2024 23:33:29 GMT  
		Size: 200.8 MB (200819456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9eaa0ea64117366d5c52182665fe7b11ec12b4781cc23d64673644613ef258f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c486980d97221ae7548b5a469d1b6cd374b74b23f5dd3b9fcd711f137491ee1c`

```dockerfile
```

-	Layers:
	-	`sha256:7d10ac2603dfc8477887351e208d3661e493820b4f77293984b5d842f9677f50`  
		Last Modified: Tue, 06 Feb 2024 23:33:24 GMT  
		Size: 1.9 MB (1914468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b651ac812c9504d5eae2e593cee96da171d36816a8dff6a7edc840b760751a6e`  
		Last Modified: Tue, 06 Feb 2024 23:33:24 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
