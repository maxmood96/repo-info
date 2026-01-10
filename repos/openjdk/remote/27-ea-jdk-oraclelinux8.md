## `openjdk:27-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:da060a5678e5e1f3df47c30e38ec1d703c0dd2b5f04a4d5020ebec7980147ea1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:4b367b88418862e16f1a278b8d95e2b5fa1179147db63edd9d4a4a8c2a3d3738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294836716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1c1034149e0b1914e3be81da0e1cd73c99e0f2d0d15bbf9f9ed628d681c6cd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:43:04 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:43:04 GMT
CMD ["/bin/bash"]
# Fri, 09 Jan 2026 22:10:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Jan 2026 22:11:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 09 Jan 2026 22:11:16 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jan 2026 22:11:16 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jan 2026 22:11:16 GMT
ENV JAVA_VERSION=27-ea+3
# Fri, 09 Jan 2026 22:11:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Jan 2026 22:11:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0ddc6852d18db715e5e4c3edd3fa8bdf8afc37b9507d95d8bc0194012c32432`  
		Last Modified: Fri, 09 Jan 2026 21:43:27 GMT  
		Size: 51.5 MB (51465737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443a4c595956fed24dda84181abe9cb07dbbe906943f80033bdad8cf5cae3aea`  
		Last Modified: Fri, 09 Jan 2026 22:11:12 GMT  
		Size: 15.0 MB (14989233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f533e9f32708ea6e03abc1d68255ff3798d88d2f3fad0f08af7e8c0459e2e55b`  
		Last Modified: Fri, 09 Jan 2026 22:11:51 GMT  
		Size: 228.4 MB (228381746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6675fc8341b6e58c930bc8a52835bd62fe3660ec7d8a10c143205cd35bf9ebb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbe5935fda6f64c41f6c20e0bd04fd25c15677786f228d1ae08ee45cccc3af7`

```dockerfile
```

-	Layers:
	-	`sha256:80613d7ddedebe1bc5ff31657db36230a257a74c8a098022480f146b1e9edcee`  
		Last Modified: Fri, 09 Jan 2026 22:24:30 GMT  
		Size: 2.4 MB (2448674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf4bf1404f8a1ee20dc16b5c6041e8296cda628160137a46594c81fa09d963e`  
		Last Modified: Fri, 09 Jan 2026 22:24:31 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:607286470e4f1cc2a631d16b75d95b3e0a920590aaa0bcec50e37a48e37286fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292215953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e56cdb6ee6caa32e7f854a199ebe59f4f7c53f2287157b12fe1fb0b5019d13`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:42:51 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:42:51 GMT
CMD ["/bin/bash"]
# Fri, 09 Jan 2026 22:12:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Jan 2026 22:12:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 09 Jan 2026 22:12:31 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jan 2026 22:12:31 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jan 2026 22:12:31 GMT
ENV JAVA_VERSION=27-ea+3
# Fri, 09 Jan 2026 22:12:31 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Jan 2026 22:12:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5daa2797aa97d66d1615bd1c3686dd694a6f5fa7082128bee108f37838f634ba`  
		Last Modified: Fri, 09 Jan 2026 21:43:15 GMT  
		Size: 50.2 MB (50181216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763332bf3d88f8914c9191bd725cc01b3ab4c117861001736c9734af68b2ffa8`  
		Last Modified: Fri, 09 Jan 2026 22:13:06 GMT  
		Size: 15.7 MB (15700566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9551d8e13b046d22751306acba9fc9a331b1cc8deccbe1be241101446605c71b`  
		Last Modified: Fri, 09 Jan 2026 22:13:19 GMT  
		Size: 226.3 MB (226334171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8c3f1770d564114d2e645bcaea5c88e3abbf2ce58c9805af99ab243a154431ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e4530cb77deecadeb6f35d8f2bb68ec09dc48bd461d6afeae63c95e83641f2`

```dockerfile
```

-	Layers:
	-	`sha256:ec043f5f833017811623512db1f1c958ca875887e56759062673101609f40cdc`  
		Last Modified: Sat, 10 Jan 2026 01:24:25 GMT  
		Size: 2.4 MB (2447484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18ee96e324f6784ed091be370580f7801c55f0e52e8805144ee5d067c86f686b`  
		Last Modified: Sat, 10 Jan 2026 01:24:25 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
