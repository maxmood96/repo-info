## `openjdk:25-ea-23-oraclelinux9`

```console
$ docker pull openjdk@sha256:e0089d90045e0910813c799ec2ceb22825a8d80a598e52e31074fae183199c1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-23-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:8ceb5b6cbbba3010c9997fec054afbace1d69fd6cefe038bcb65796a65c880eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300626316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8528bc23259617e4e2898924cfe05835175ee8bc67321aa05a2088d76e18e499`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:26:20 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:26:20 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2eb5d06bfeaafd2195d3612935e86f925a4620bf5bbcea5112a1fb07138dd80`  
		Last Modified: Tue, 29 Apr 2025 18:16:07 GMT  
		Size: 49.1 MB (49093011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a66751aa9c49152f72ba7e023ee706c3024d864e1ca802a2cf161456c51a7f8`  
		Last Modified: Fri, 16 May 2025 20:54:21 GMT  
		Size: 38.1 MB (38107572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d4ee174503292e5bc0d00c0d6797f7425a867c918890af41bddaa23cf2787`  
		Last Modified: Fri, 16 May 2025 20:54:23 GMT  
		Size: 213.4 MB (213425733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:8d28491c60843ff1d478a2b02858b8205104802e0f9f0d275a9022bc3b0a0bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3654163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a563bbb2a1b7160d01f93655af78764474a45b7cae8b59b536a050eb59e6af8`

```dockerfile
```

-	Layers:
	-	`sha256:a27e3141b747f4781b12dddc38cdff786347c8e3eb3a89850f0ffdb345011ee4`  
		Last Modified: Fri, 16 May 2025 20:54:20 GMT  
		Size: 3.6 MB (3634418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b4c07e9135b02e2f25aa6238db44426e1451c58e95ae9423542e958d1cd94f`  
		Last Modified: Fri, 16 May 2025 20:54:20 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-23-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:71b8c838554d40dd4072ccc30cfd3ca07b17fdfec8e5f80df1f91daa74cc6915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297375109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4482d5cab7821aef0cfe199f2d70bf794b21f68610be4f612e140441dcd4683f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:27:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:27:11 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88a33dc8906274baf54eb28aeefeba84c17922e3854e6fd41883f273d87d330d`  
		Last Modified: Wed, 30 Apr 2025 01:59:51 GMT  
		Size: 47.7 MB (47672989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b5aea1d0deca854a3762f4e396dad66260211f50004210a8e73e2146af926a`  
		Last Modified: Wed, 30 Apr 2025 07:05:49 GMT  
		Size: 38.5 MB (38500810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7d60179c9c55aa630b975f674dd338de2477f5cbfe77d23a6729e6fc063b00`  
		Last Modified: Fri, 16 May 2025 20:53:37 GMT  
		Size: 211.2 MB (211201310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:e32d273d2166932fa572a296e0595917c399c454619d161cd5c301e2c648b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3652213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003ba166e341a5cf30a79e13ba2cbf3307e2f06c597b0815ae30c9e6b709f16`

```dockerfile
```

-	Layers:
	-	`sha256:7f26171943669cf4e33666d6730f6fa96ef3149cf0ce585c4346c46b7eb7a003`  
		Last Modified: Fri, 16 May 2025 20:53:32 GMT  
		Size: 3.6 MB (3632180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6bee1c98c7fafea6731ab28492eaa247a9e768136eded35ea699276a75c619`  
		Last Modified: Fri, 16 May 2025 20:53:32 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
