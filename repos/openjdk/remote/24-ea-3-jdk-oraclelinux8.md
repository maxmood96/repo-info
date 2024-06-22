## `openjdk:24-ea-3-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:ff181cab8f221baf7b9baf23fbb6b331dda1b316e4824eb5b3e4ba548eafe4a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-3-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:96a119ed7bc92c9ab5e8a66275ce80cde19e5ff29d845e2460620cc6460116b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278051051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecb5c0c47f9b6cd9ac40523d12f90f61fd6e0ed08f936c9e3a03a9d660952a9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:53 GMT
ADD file:6f8c3cf297caf3b2a501a32c94a4fc0d2c7024f63d5e4b2215730b56faa6cdfb in / 
# Fri, 07 Jun 2024 03:48:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 21 Jun 2024 18:52:10 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:52:10 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_VERSION=24-ea+3
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='dad750c864049dba95a01fa89ad1c52c3b702ba87c3c865e5e64fa624f9e3de0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='4a5515c226db56008676461bef7443163ccfe369415342136b8d9691ecd5130b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:427bba466fea4df7396a02ec368c5aa24d07ac80d02aa94eb57ba7af7b84b5a3`  
		Last Modified: Fri, 07 Jun 2024 03:50:01 GMT  
		Size: 51.2 MB (51219315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fa1537994bfd33f6c129ee4e2f0fca7df15dc3dc5eb59fdfc45489503afa7c`  
		Last Modified: Sat, 22 Jun 2024 00:56:09 GMT  
		Size: 15.0 MB (15035353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c03d888210ab0be8772ecd4d54ccbdd7fc3d7605ef4f2fd3e7800812624fcbb`  
		Last Modified: Sat, 22 Jun 2024 00:56:12 GMT  
		Size: 211.8 MB (211796383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-3-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6b0569ea9d518de8ed8ab98e92d7e4e48519f4712bbf15662b02d3bef91d6016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78697444535690126eafd9783df76daf2dc9fabf1cc8384de76cfad1060d4035`

```dockerfile
```

-	Layers:
	-	`sha256:a3f9dc46688640cff4ebb305f3ce412df2ac337afbc86b47c798625d16cdd333`  
		Last Modified: Sat, 22 Jun 2024 00:56:09 GMT  
		Size: 2.3 MB (2267551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bfc9a1aa691cea1d9510de74aa62d26dd484221ecfb2c886a0d3dbcf123fbf7`  
		Last Modified: Sat, 22 Jun 2024 00:56:09 GMT  
		Size: 15.8 KB (15803 bytes)  
		MIME: application/vnd.in-toto+json
