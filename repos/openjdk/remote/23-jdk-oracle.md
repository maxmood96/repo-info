## `openjdk:23-jdk-oracle`

```console
$ docker pull openjdk@sha256:6c7a10ff322d2bb6ee2f3c2fed5f0a85ffd7a355219090bd0363ad1215aeb700
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:12c90e5b56a5f905c03abd1358f865e09f21cabb5644b73e282122a1582bad42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269471060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0971c90bd6e5933b2b7fe703b5135f515b320b7bd9116fa8e4fe734058f74fd5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Feb 2024 19:54:38 GMT
ADD file:cbc540158e77b85113e3a0e0ed1e202046cf293cdb8d7cd890b04883493dbf35 in / 
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81badc5f380f1ca21f6c430303f4107b9b5e0af27c59e3725bf731915b457fc8`  
		Last Modified: Wed, 14 Feb 2024 01:49:17 GMT  
		Size: 51.3 MB (51325575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8a5871e79e5573516df42223f90bbbcfa65e9a9eb2598465b228da22bfbd9a`  
		Last Modified: Wed, 14 Feb 2024 02:56:02 GMT  
		Size: 15.0 MB (15005903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d1a00f29dcdc7c678e0d9942c69b9fd51fbb7c607045f72fed98005e162e2f`  
		Last Modified: Wed, 14 Feb 2024 02:56:07 GMT  
		Size: 203.1 MB (203139582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1c2a8ff62fc67d9e24037e38794fb83e02b227a99ad546cb0778ad4f119ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6aa1e93d7047e3043b46b1c642be1e1629d88f411f9ae2020e2ae0fb9c71bdb`

```dockerfile
```

-	Layers:
	-	`sha256:8f2b4d58496794abca998df6d24b78017d82df69d257cba2472d24ab10008081`  
		Last Modified: Wed, 14 Feb 2024 02:56:02 GMT  
		Size: 1.9 MB (1915878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d0f312638b01840281731bada2f14351ddb8afca690c09e0a6d3ee7fa7b0f2a`  
		Last Modified: Wed, 14 Feb 2024 02:56:02 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a5441432d41979667198c7eab2078676fc3d335049571e701b18fdd96e2caea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266790628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd13790579cc2016ef91825f4626a1461c7390346b9ac9e2244362c19bf0af1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Feb 2024 19:54:38 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04d3eef9c8a6237c8b46c9794501777a8ce3c58a2e3a645da53db98f8e028aa`  
		Last Modified: Tue, 06 Feb 2024 23:32:40 GMT  
		Size: 15.7 MB (15691300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0424db6fd54da4ee49352da540b5250d76379f7279f50cec7958457f53c7dde`  
		Last Modified: Tue, 06 Feb 2024 23:32:44 GMT  
		Size: 201.0 MB (201021904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b7ee96a1bbe686cb2570fd0394cdca7941ba32f804c2b8c316f26baf5f6a9553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69d716134b62756e5453c94b9c86a26da12b3896eb05bea29bd958a6867f18b`

```dockerfile
```

-	Layers:
	-	`sha256:d1cbd353423e75b2e038d7dbd4e5754cf5d44acf57b2661fee65673a34deef42`  
		Last Modified: Tue, 06 Feb 2024 23:32:40 GMT  
		Size: 1.9 MB (1914456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc2a941c7d52455658f6cb481c7cc1b46d3824f2b2aae0ac3002c33eec55f32`  
		Last Modified: Tue, 06 Feb 2024 23:32:40 GMT  
		Size: 19.7 KB (19734 bytes)  
		MIME: application/vnd.in-toto+json
