## `openjdk:24-ea-12-oraclelinux8`

```console
$ docker pull openjdk@sha256:71cbe149df0f62dcb042e9b2bc027f0e5e2ae9975c57c21d0469490d06154123
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-12-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:54ff2f82775bd6d531470b4de7b0fc03d0a77fe976deb80515aebbc62e1d979d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278648799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c6bc9301c164358818267734705dae209d19d480842eef21138cef1a339521`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 00:48:14 GMT
ADD file:31fe8501106347a4e3341c03d1b81904a23f97e8744fdf62f24355513658cb72 in / 
# Fri, 23 Aug 2024 00:48:14 GMT
CMD ["/bin/bash"]
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 23 Aug 2024 00:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Aug 2024 00:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_VERSION=24-ea+12
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='9a859e4f3840e3f0890051a26b06413cd18dc8a1b7d68b221f47b38ba2f5add4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='4631ab62c58dbecfc00983df819c9a669b3d4fb681d7f6c3d95af11b7aacf087'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a4c7d85dbdbfdeab6ad5b1244e378081e17343d003de892c7fee8d9dd53a329f`  
		Last Modified: Fri, 23 Aug 2024 01:22:40 GMT  
		Size: 51.3 MB (51294233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259bd517fec824377dc69cc4013c2db6b4a5bf2cb7a315bc6591303aafd9ee54`  
		Last Modified: Fri, 23 Aug 2024 21:11:13 GMT  
		Size: 15.0 MB (15040962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af8195f03cdca65ff79966795cb35fdcf86e0ba9d8d6f7856d20ba8c89f0f2d`  
		Last Modified: Fri, 23 Aug 2024 21:11:17 GMT  
		Size: 212.3 MB (212313604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-12-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:df1564c6c63d0fc42408c2c73b0d752dbe508992a88b5d647a6ea403511ef8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125e46afdf4176e1b3d5851f2e656fbef26c991c0bc8af236da7e6d1c013a9a4`

```dockerfile
```

-	Layers:
	-	`sha256:42e35674e6e810eb095af726e277aa6c4b2fdbaef70d958c4faca72ccbf3a8c8`  
		Last Modified: Fri, 23 Aug 2024 21:11:12 GMT  
		Size: 2.3 MB (2287869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6527bef175be29802868e56195d6d5aa424a9690c4ac9556189e0d79c6715508`  
		Last Modified: Fri, 23 Aug 2024 21:11:12 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json
