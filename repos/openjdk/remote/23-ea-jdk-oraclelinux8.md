## `openjdk:23-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:e2dfd973db92050b5dfe71f0b97b1b8cc3e892686a5e63f22ea19b8bd48129d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:77646f3f4aedaca88fb0b2675f8cf0bf99c6ae2f4c3dfca2ce514bda52f15e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277192600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b722f87e51d3f1fef7a60dfb6adb0ee9db563847b78b93055803a4565a1909`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 May 2024 17:23:46 GMT
ADD file:8f1e63c197fd50c6b0e1841be870ed49e0149654eb523d4ceebf9dbd1c9eaa92 in / 
# Wed, 29 May 2024 17:23:46 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 29 May 2024 17:23:46 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 29 May 2024 17:23:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7739e1b0a17a1112aae4b01fa39d979aa72dfa002be5059a8488942f3c2753fe`  
		Last Modified: Sat, 01 Jun 2024 00:50:45 GMT  
		Size: 51.2 MB (51220385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8933669d0ea6c2a811f3654d981afbc6bc01ce46a2977f6273cbbb0eccf84e`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 15.0 MB (15031231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8206712825caace49fe27ec1828846d76890e8497b15da707c05140af50056cc`  
		Last Modified: Sat, 01 Jun 2024 01:50:33 GMT  
		Size: 210.9 MB (210940984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:15997e0bfea9db6769d407dd665f8e37f9380e061d78a1b32e4a737580fd944a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c22b6fabf586d96c48b0be8d5c8447b1582d2debca80e8e891509f3ee292be`

```dockerfile
```

-	Layers:
	-	`sha256:6d5be694e156b6ce63b1594edc6e1193b50154cae61336b0ea78ecb0cac6acff`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.3 MB (2267552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5865eb38ff4d42f99a0e85eaa7ff113adb5e18e5c006442fdba9bc88ed3ccda0`  
		Last Modified: Sat, 01 Jun 2024 01:50:26 GMT  
		Size: 15.8 KB (15771 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9fff9884a184e3a3ba2dcf9a81ab42f72e4148f546fa89c7f771964b35b06884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274623160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fead88260d2f01f2b4cf22b5a7e4ae9e3fff71390aad6077f9e18bc4123a40`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:06:44 GMT
ADD file:603b84a8cdf20851437bb944c9946c0ac32645e0e0946ffebf3ed5ad10c141bc in / 
# Thu, 09 May 2024 22:06:45 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 29 May 2024 17:23:46 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 29 May 2024 17:23:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8999f2c02994f155685ddf5b1c0822a620022aa57946ee7ba5c754261052b2dd`  
		Last Modified: Thu, 09 May 2024 22:08:16 GMT  
		Size: 50.1 MB (50082252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5dd36508000838d650120d4ddcfcb431dcb09b64b708c6ec0b7946279e9cfb8`  
		Last Modified: Thu, 30 May 2024 12:46:04 GMT  
		Size: 15.7 MB (15699223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05332e10cd1c493df9d6216405f969b77dd033227687a65a500045a6eb539c89`  
		Last Modified: Thu, 30 May 2024 12:46:07 GMT  
		Size: 208.8 MB (208841685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fa70b6d6b37ed9feeb6fed87afa3a11eba16fc9ca051abf6c6c48e1bef344f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afefa3cf57b587c047d4a697f42b29f38391dc9be703d005714b7ae0f9a6e97e`

```dockerfile
```

-	Layers:
	-	`sha256:cfe802f0b24816ccb9c6996f3745df0607da7403312621fd8f13cabda22ae3c0`  
		Last Modified: Thu, 30 May 2024 12:46:04 GMT  
		Size: 2.3 MB (2267056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddbc19a31041b04819e20a52aaf1d02d4e3b717a8479bad43fc7cff31d9fe721`  
		Last Modified: Thu, 30 May 2024 12:46:02 GMT  
		Size: 16.1 KB (16102 bytes)  
		MIME: application/vnd.in-toto+json
