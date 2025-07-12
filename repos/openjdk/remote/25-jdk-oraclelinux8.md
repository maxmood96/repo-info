## `openjdk:25-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:19c62157c5d9d8b7493504072faafeb00378b7524cfa2d6523810fa5f58caffe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a76084e67ff7b7e5fddd9777e74a566ad91504fd9e9f495e47042de487c2cc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289817473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5553f76758fa8d70c22c31d9aa07bdd9d3e2b2a77323f53ea0540bfcd8cd571f`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:48:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
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
	-	`sha256:41875d08ddffe10cea627347ab2d190e7a42649b4f26f96bcb1236b617350f27`  
		Last Modified: Fri, 11 Jul 2025 23:03:01 GMT  
		Size: 51.3 MB (51312999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25943c64254056037369b9b73e791e25b0bd09f4b43ab3578797d7ebd5a9e4bd`  
		Last Modified: Fri, 11 Jul 2025 23:08:41 GMT  
		Size: 15.0 MB (14976369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9cf05542117e6ab596b4e134439efa0f28eada9bba553a161e7b8285aa7c41`  
		Last Modified: Sat, 12 Jul 2025 00:32:05 GMT  
		Size: 223.5 MB (223528105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8666af9669126c982279a0fd64856b7d3c67ee97ae83c368f704d791e926213f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b006169a78c1be17385712bd9e119f0d81695a7bd362d0eee3b569f07930e9`

```dockerfile
```

-	Layers:
	-	`sha256:5b81e05a6bce7c4fe0b0bae700242e062d5bdc66a4dcd0502475dbae1f94f2d1`  
		Last Modified: Sat, 12 Jul 2025 00:23:27 GMT  
		Size: 2.5 MB (2451710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930913fe7fc6b4dc53be870c46c20e363421f714e8365240ed9574ce909988a7`  
		Last Modified: Sat, 12 Jul 2025 00:23:28 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:eb4032563e2093bd242c2bda3517f0b574db730016d2942b6ad91d6deea949a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287049631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0164a751c5b536f7fbabdcae6f1ddde23b8c10b97d53870fc28079fc601152`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:48:10 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
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
	-	`sha256:4dfe820c20154be581827f07570596df525d44687f95b28b72c9da6274369d45`  
		Last Modified: Fri, 11 Jul 2025 23:27:02 GMT  
		Size: 50.0 MB (50031150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2354c264baf5ced06f90feda02f9e83f83a23da58b709069976e09fca065d12a`  
		Last Modified: Sat, 12 Jul 2025 00:01:45 GMT  
		Size: 15.7 MB (15680450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd789e5d38270f92073b906b9880f2f163591e99ce4f449068f1e1d125d6873`  
		Last Modified: Sat, 12 Jul 2025 00:32:12 GMT  
		Size: 221.3 MB (221338031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5a4374de940118e999b9a686e951960985bf00bf724ef57a86f16d4bcd60945a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5be4fe18d92921fe4d74cd18741695c9c5baf0b46dff58bb908d1d1d1f7de3`

```dockerfile
```

-	Layers:
	-	`sha256:e890e916fa3c4c3ae0169e38ce3aee60f594802f896e526b7c7929aa99691f61`  
		Last Modified: Sat, 12 Jul 2025 00:23:32 GMT  
		Size: 2.5 MB (2450544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464b53699edfe9bd1b739d5e50019648d0057009726190f454a15b2e3c6aea05`  
		Last Modified: Sat, 12 Jul 2025 00:23:33 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
