## `openjdk:24-ea-1-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:dbf2ad3f999111b2cd70daacda8fac64a4774514e2a81c82fe01d8b3eecd6d75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-1-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:fa0270adb1a502dd8caf32d6c9484c5a49b6fd7b30f822923a55a662b3eb66a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278061625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60012a41e7152eeb14c8f95a139b82fc20b8e4873bc869997612019926b9e83a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:53 GMT
ADD file:6f8c3cf297caf3b2a501a32c94a4fc0d2c7024f63d5e4b2215730b56faa6cdfb in / 
# Fri, 07 Jun 2024 03:48:53 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:427bba466fea4df7396a02ec368c5aa24d07ac80d02aa94eb57ba7af7b84b5a3`  
		Last Modified: Fri, 07 Jun 2024 03:50:01 GMT  
		Size: 51.2 MB (51219315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3450faf8daa5813d60168f69c0f215b898dc7dd316a7b99fee60584c6dbcbf92`  
		Last Modified: Wed, 12 Jun 2024 00:55:42 GMT  
		Size: 15.0 MB (15035462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2efa40314a48479606bdca27f1979bc853e8ab394fe94a0af7f2a6a34ee60b8`  
		Last Modified: Wed, 12 Jun 2024 00:55:44 GMT  
		Size: 211.8 MB (211806848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-1-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7a830443172828f36a0ad3a42c8249ae2160bdb4bc34bbb35d94a4993189ea5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7716e3e23ba1e84da9bbb56b2ee87e688eb2a5acf093a0111c52f3021524a5`

```dockerfile
```

-	Layers:
	-	`sha256:6c448b700ace568eef16e2da3274c395294b90457d3ce870be613409d5b24067`  
		Last Modified: Wed, 12 Jun 2024 00:55:41 GMT  
		Size: 2.3 MB (2267548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810279a75c56e3cff849dd070fb2219ece45f27abd7c4a9613febcc2d9bf7d31`  
		Last Modified: Wed, 12 Jun 2024 00:55:41 GMT  
		Size: 15.8 KB (15803 bytes)  
		MIME: application/vnd.in-toto+json
