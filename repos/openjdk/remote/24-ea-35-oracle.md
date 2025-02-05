## `openjdk:24-ea-35-oracle`

```console
$ docker pull openjdk@sha256:8796400cc40bfaff4f96d3934e60fca4e0bae9cdbd6ad2b2aa6014c08a31aef0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-35-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:e34330622dfa3388f2b9a436afd0b10ecc394f9b8b6c87ff69b8d21892c01f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310713568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664eb4475f2d7dce32ec2c59778fd3d929c40baa46a4a6a164f2d40f7565d814`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e13c2c6724045c9467bfca098ec9db486930a494c29cfe76f9b6f76e395d2b4`  
		Last Modified: Tue, 04 Feb 2025 23:32:59 GMT  
		Size: 48.8 MB (48774772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d27cddf9546467c2f04ca8e03d71b2cf4ec412f5950a65aebd20c2f2b2d027`  
		Last Modified: Tue, 04 Feb 2025 23:33:02 GMT  
		Size: 212.8 MB (212840094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-35-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:359430fd2c716eef17e9e423e493997dadeba9b7f2481ad05e9595f84a810462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0cc76712ed14b99aba83096455fe8497da8b9ccc962394bc462df91c7ddc24`

```dockerfile
```

-	Layers:
	-	`sha256:b16b413cf4313f39b324d6afe39c5855bacb7e8b27cab5781f566d43765275b8`  
		Last Modified: Tue, 04 Feb 2025 23:32:59 GMT  
		Size: 4.9 MB (4911329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a8683f86f0ee5b8abf7d793b54e0dc9da42fa045cad5f121ef69c7984171b8`  
		Last Modified: Tue, 04 Feb 2025 23:32:58 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json
