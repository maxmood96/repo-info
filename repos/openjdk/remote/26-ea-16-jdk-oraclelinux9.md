## `openjdk:26-ea-16-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:0e2870ca0750406576d5fd34b558124bac3f835930cd402aa1c61107cedbeb80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-16-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2e157edc9b0eb4f2def59c9cdbd5fb1089604122e1d68517665734cf3d656c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307780096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6066d45d46f81ac53132e0619f3de33f6e1ec0ebf503ac88e057ed69953cd53`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 20 Sep 2025 00:48:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 20 Sep 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Sep 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+16
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='87ee3d9cfd07f66858b6e519b07d2f23375fb1c1827faeebce6580c31045879f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='116ea44265700afbfe2c15b751ef9e34921fa449663ac0dfb439adef9db9c379'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ced48bfda3c88462c42fbc52f44e23314673e78a25a1ac9998494789919ca`  
		Last Modified: Mon, 22 Sep 2025 22:11:08 GMT  
		Size: 38.5 MB (38490225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e8ae45614697f1763ba9a45df2879272de94e33ada887f42c34f3115f2fb85`  
		Last Modified: Tue, 23 Sep 2025 00:24:23 GMT  
		Size: 221.2 MB (221201574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-16-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:34d9c76b01991c7e7f45cc3fbb64f7800b6af1706ffe45c89c7b031f9dbfdb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9c7b725229cd5559a84392d18a3adf316bc8033d2c39d2546c923bd1d837f7`

```dockerfile
```

-	Layers:
	-	`sha256:95bb26bfc9be2c62d26277a23d6a1791cd7f013d76d63cdf1909d10183ccea3a`  
		Last Modified: Tue, 23 Sep 2025 00:23:27 GMT  
		Size: 3.6 MB (3638499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881391057b32f455b1fd55e4d5b55cbb09fec6eb203a1b00e624176780421afe`  
		Last Modified: Tue, 23 Sep 2025 00:23:28 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
