## `openjdk:26-ea-12-oraclelinux8`

```console
$ docker pull openjdk@sha256:d6f11d6de089f6710b5134ae02a571caf10b2145a8ee67eb1099d3015accd101
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:26-ea-12-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f6a6edd942f6c8395776c4f72ec860e7a74cd40ad6911a559ebfea3f6c936c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289844005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91ce66ae938d1604fa0fa2b6c406de383579eb0a44bd0e3d0da3f2287e4f2f4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69cbe7a14572166ede7e02155a84fa3a0c6bcee30ccdab53ed579a8808d3f2b`  
		Last Modified: Mon, 25 Aug 2025 21:44:49 GMT  
		Size: 15.0 MB (14977046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610b5b12274d85d15902bcef2318803972376a68829b5f84627dfd47f5d9e6df`  
		Last Modified: Mon, 25 Aug 2025 21:45:04 GMT  
		Size: 223.5 MB (223543396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-12-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:166302a5312035ab5bcb649e91cb7eb38d2b226f8abab9e7c339ae938866903d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd83e1d6f43ce3ebc28a9ad7702c5a006099dab40684e63fef3aab94ee69cb8c`

```dockerfile
```

-	Layers:
	-	`sha256:f77d462897a507506766dc00641981a3d2e68d54c9ae39052b0daff3fbb48620`  
		Last Modified: Mon, 25 Aug 2025 21:24:07 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b99c9f338cecaa2c3d099c9ad3cef37adb5616a5c0b8fc054040bc664d786284`  
		Last Modified: Mon, 25 Aug 2025 21:24:08 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json
