## `openjdk:24-ea-11-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:2ce9e3766310a8227315c75ba139bfa7fe9711a8988fef0631d05e70e4ed6340
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-11-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:113530aa1862a2b3325f18dc0537bda38cb529a70f052df30e9699c1b55fabde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278558241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c859631cdeb322388e0dc7366812e20c20f435e3c7e43149346e25839dd4ad4b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:31fe8501106347a4e3341c03d1b81904a23f97e8744fdf62f24355513658cb72 in / 
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["/bin/bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a4c7d85dbdbfdeab6ad5b1244e378081e17343d003de892c7fee8d9dd53a329f`  
		Last Modified: Fri, 23 Aug 2024 01:22:40 GMT  
		Size: 51.3 MB (51294233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde828e1e45209cc4778898cb8264f77b71e57977177d13b382ff49b5e066eb`  
		Last Modified: Fri, 23 Aug 2024 01:50:32 GMT  
		Size: 15.0 MB (15040867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e075e50bc3bfed2bd07a6d28e2c8054d8bd6a8e1bd4047417cde0c3f1b47338`  
		Last Modified: Fri, 23 Aug 2024 01:50:37 GMT  
		Size: 212.2 MB (212223141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-11-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d595a61a444906eb92f6a9777f10bdb835fe2f5cfa56589c43fc4497ce3226d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2616b95a9a48c8b779ddae129b0daaceb6c3c1201f4db89ab65009cd7b531`

```dockerfile
```

-	Layers:
	-	`sha256:96e3906bfca3e667afd45ca00cb1b1ab66af858e22fa7158b7f515958aa61cee`  
		Last Modified: Fri, 23 Aug 2024 01:50:32 GMT  
		Size: 2.3 MB (2287869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7e413379b782d69aa31643400778bf198940ee22aa946e6340db6042114c50`  
		Last Modified: Fri, 23 Aug 2024 01:50:32 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-11-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2d43c79f12aac8c4399fd59cf827e74d8b32bb2f9f21cd2f9b2ace95b68dbf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275782671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831967442f5d13d385a00b461ebc0348740ac61ccb44ab27e2150bded29514b0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:6b13879bf605622e279dbcac5c590af19f2ada3a9a83051585288eac41ef5a5b in / 
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["/bin/bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee4bb281b07b90a8d48b631141dbbfe6ee3f5d88680eac4b43c59de36db45ca5`  
		Last Modified: Fri, 23 Aug 2024 00:42:25 GMT  
		Size: 50.0 MB (50007867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f312e00b787dbc2b511697306ec64b5bfc43ad7382974bf128f204ebae9d1242`  
		Last Modified: Fri, 23 Aug 2024 01:56:06 GMT  
		Size: 15.7 MB (15702871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05078d388493ef0e48e4dd650b53c9312d0b4c847162405680d4df92f1ae06ff`  
		Last Modified: Fri, 23 Aug 2024 01:56:11 GMT  
		Size: 210.1 MB (210071933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-11-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:3c909fce052568715bfb398ded53fecba945df8b47cf3524f1d83ce42e2bb5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe563a102ff87097dec69e7eddaf0c71596c4874cf990be90343d88b49ad8bf4`

```dockerfile
```

-	Layers:
	-	`sha256:c7111bd375f0068d479b097a39a2b3cc25ace7169090153594305a675d45a006`  
		Last Modified: Fri, 23 Aug 2024 01:56:06 GMT  
		Size: 2.3 MB (2287338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80556647a61ef5401e33e97cce595742443b8d1c24136ad8a4450cdaff95e6a3`  
		Last Modified: Fri, 23 Aug 2024 01:56:05 GMT  
		Size: 16.1 KB (16149 bytes)  
		MIME: application/vnd.in-toto+json
