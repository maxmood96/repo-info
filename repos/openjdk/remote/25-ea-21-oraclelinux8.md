## `openjdk:25-ea-21-oraclelinux8`

```console
$ docker pull openjdk@sha256:b6340c965fdf1932a63cf7a8956feefab3e674ece6eec33d0151351ae755a061
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:25-ea-21-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:cf31887db638230e488da537128b9b85a27f8ab634c10b4c9c3a1dce13639b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280077874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b1952c0000a2ed5df2337c598e7d3ba28701c6d7db41cc13401eff0865e630`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:19 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:19 GMT
CMD ["/bin/bash"]
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 03 May 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 May 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_VERSION=25-ea+21
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='9215df470d2d44c8ea731dcde9e170b6951e29f6e96e90625be983f0f9cfd1ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='23b6cbdac4dedcb1e7d290e7f5e9da01be8c4dcc35b4d296054aae3588d4465a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 03 May 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ee6d2b4bc3292763eeab29f03adacbfcd179273f648dc332abeb3f2f9cf99a3`  
		Last Modified: Fri, 25 Apr 2025 22:19:54 GMT  
		Size: 51.3 MB (51312878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218eb0a34daa41fb3015241231840e3f7bf25cf462cfb7f8d70e6873ee36a558`  
		Last Modified: Mon, 05 May 2025 17:30:38 GMT  
		Size: 15.0 MB (14998163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd29c5c2a44a5ddd1ff5ad53310f3ea1784cac82bd5cf43ec8eae16b5593909`  
		Last Modified: Mon, 05 May 2025 17:30:44 GMT  
		Size: 213.8 MB (213766833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-21-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:726b5a0b7e8e6936102b22c12e71712a83106063b14540756b1e2f8be334f4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4124ed8b37a982ebfa9ca0f7f035c1b9bc14e6e00b24641e2e406875547862`

```dockerfile
```

-	Layers:
	-	`sha256:4a3aaf910f6afc2413dd7c3f4b15dd13a8a1619725651632e9025c9789704b34`  
		Last Modified: Mon, 05 May 2025 17:30:37 GMT  
		Size: 2.4 MB (2442873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec37e2e9d3063c5a2c5848303b815d52c8bbea63a4b1e6b85a49e3cf755e170`  
		Last Modified: Mon, 05 May 2025 17:30:37 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json
