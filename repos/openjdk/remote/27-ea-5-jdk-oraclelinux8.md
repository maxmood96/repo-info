## `openjdk:27-ea-5-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:f190871218f5d5c27757129bec1ac2dd5b7261aab6c9f57d96460a4a911695fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-5-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:baaf2d0a5882490ed4617b180dee867375699d725b39191298468f197feac608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (294989317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a21a6ab8c591da79e3ecbba25b446429a28712ed829e49b08847cfa3f219239`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:45:16 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:45:16 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:48:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 20 Jan 2026 18:48:20 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:48:20 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:48:20 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:48:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:48:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9c709a374865394632aa738429a90691dd8d7699af8be91820b62e8c54881b2`  
		Last Modified: Fri, 16 Jan 2026 23:45:35 GMT  
		Size: 51.5 MB (51468262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5c9e53195453d7569c2235b4107ea6bdb65f759ab4ec6297c69473304c78bb`  
		Last Modified: Tue, 20 Jan 2026 18:48:53 GMT  
		Size: 15.0 MB (14994014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e430a5060618c9e737a287bbd7d075a1c60f41194c9150f3edd68eeaec935f4d`  
		Last Modified: Tue, 20 Jan 2026 18:57:59 GMT  
		Size: 228.5 MB (228527041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1175ee056c4d2ea79ee6207dcf742d5b17963dc441e129cd315832a60f1e1747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5075a2b88a011bb0b84da8bcd8bace817a9ebd2cce0b08b358ce91e27d6a2c08`

```dockerfile
```

-	Layers:
	-	`sha256:fed0fc713c7ed47f320cca4c20fb0506f7207ea211b9106c2c2f5c729099978b`  
		Last Modified: Tue, 20 Jan 2026 19:26:15 GMT  
		Size: 2.4 MB (2448676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacb0308532b267924ee37116173ee183a946148466c690a0aa414a829ae34f5`  
		Last Modified: Tue, 20 Jan 2026 18:48:41 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-5-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8f300b6348e55e35b14dc6a8cfebb1a72a7fabac41b6948d7f19dc42e73963f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292372133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f08479746a5c7dc56e984a8224a405593d6ce1f488c36e34a6539875ad24716`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:45:22 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:45:22 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:48:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 20 Jan 2026 18:48:37 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:48:37 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:48:37 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:48:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:48:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d32cf4966caecd91a10183493338f37f77a209057fd98d8c3aff049ad44e3619`  
		Last Modified: Fri, 16 Jan 2026 23:45:44 GMT  
		Size: 50.2 MB (50200257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1813f57b46cdd9f53194bf4f94e5f6e52bd7e0d92cecba188127bf3dc25121`  
		Last Modified: Tue, 20 Jan 2026 18:49:11 GMT  
		Size: 15.7 MB (15692706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e737052c565930361591cf472964ea38fc6926ce071765c7ec2188ce59043df4`  
		Last Modified: Tue, 20 Jan 2026 18:53:24 GMT  
		Size: 226.5 MB (226479170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b52c548801c009f7125892a258ce497c9032c17af5be9a608483bf03cd8d3c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7f017c3cc32850aeef36c6b7ac99ef8501aca1f0442f2a560d5a61314d54ed`

```dockerfile
```

-	Layers:
	-	`sha256:2d8b825904b7fd45dcc12325bdbc621a061203cbdf5bdff0d4d953f2e92751a1`  
		Last Modified: Tue, 20 Jan 2026 18:48:58 GMT  
		Size: 2.4 MB (2447486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73afb35e048f322779ca1b590ba461a084ae759a6c37d9829f8b36b7b877a8d8`  
		Last Modified: Tue, 20 Jan 2026 19:26:36 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
