## `openjdk:25-ea-30-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:ad389c716c0ff019030a91a1cc57fdf6409e908027f2c14f248da896d1294ba0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:25-ea-30-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a6f3ac917769f76e4c86fa7a88bb4dbb274fc8ac6501f0ab9a800649ea795ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289816684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4cee790532365099332c605e8748dc60ed0e2afc36d605ff8e1e1ad8d7e3e4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db68233315b339ed378537f7eb43e70bccdc0c2bd9c82436a03212fa0caf94ad`  
		Last Modified: Mon, 07 Jul 2025 21:34:02 GMT  
		Size: 15.0 MB (14979351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e232b0a04509e2fcd64cbef2984728e4f5284184cca1757e26acdec988813`  
		Last Modified: Mon, 07 Jul 2025 21:34:22 GMT  
		Size: 223.5 MB (223525775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-30-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5dbd7d30b224d4b457d332981f0e92f93b9ae9e606bfb79e99c2d9e98c9b0c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24898e085022b2b77e36244459a783986f110c170c3e005c18a2a2fc875c0130`

```dockerfile
```

-	Layers:
	-	`sha256:375d3772435e75937d29ec80dc17f5ba191ff8c4d24ec81f55fa9d48e1bb80a1`  
		Last Modified: Mon, 07 Jul 2025 21:23:46 GMT  
		Size: 2.5 MB (2451706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec36190586fa4f5863322a1db0f6722ffd63be5158ebe5c8274ec59ac57aecf8`  
		Last Modified: Mon, 07 Jul 2025 21:23:47 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json
