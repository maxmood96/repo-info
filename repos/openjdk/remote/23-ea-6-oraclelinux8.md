## `openjdk:23-ea-6-oraclelinux8`

```console
$ docker pull openjdk@sha256:4b43c38bae129b451bc194c40c787ee47f5c03a41d68938457cf91101a129f18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-6-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:e5b07eb778fca749452a5a7d87d861339483cc6584e910a7d9cec43d91741a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269370397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5952b826704bd440a58118659769fbf5e6128f80459ef67747d9cd0b712d421`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Tue, 23 Jan 2024 20:18:23 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 20:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_VERSION=23-ea+6
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='5163a8a077bfb1cb60e6b4ade06959b0ecba73399a509a5e83f8f9df5cebd140'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa7e954bb29a17c5d0095c4ce94275bfe53383cb8aa7f14894d352e9c00110c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fd9bd5585c598a715bc18ed5e3de491dfd601818bf86689a52bbea1427ca6e`  
		Last Modified: Wed, 24 Jan 2024 20:50:30 GMT  
		Size: 15.0 MB (14991042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf89b269a940f18d906c500ac4fce1c22657256faaea2e6625d09063c004cf8`  
		Last Modified: Wed, 24 Jan 2024 20:50:35 GMT  
		Size: 203.1 MB (203057624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-6-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7e694aad34527225b5b504b858ee8104b7eb0b38b5f1a982d7fa1954dac0787c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8140945d528febbd053c7c174c53a1d5f7da344f25bc76714e18fae4a4cd9b1`

```dockerfile
```

-	Layers:
	-	`sha256:1a03e2aaafd4d750faf9b1f195df997356160c8e150ee39a75657530ce4ceccc`  
		Last Modified: Wed, 24 Jan 2024 20:50:29 GMT  
		Size: 1.9 MB (1915843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa556ee04f024ead7d4de61b41b26e9d52be46076cc13ebd1aff1eb409ed7132`  
		Last Modified: Wed, 24 Jan 2024 20:50:29 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.in-toto+json
