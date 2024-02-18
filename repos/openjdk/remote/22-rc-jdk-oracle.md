## `openjdk:22-rc-jdk-oracle`

```console
$ docker pull openjdk@sha256:d8dea2a4cb6519d2b5b2b41bc798ad483d8f047ff28d4e0d41a2d0d240101906
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:0b8632bb0e96fdc84f8a31a0b6fc2a53d9cc1d44d61395126e6e76f23fbc929e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269099615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b9900d2c523e1a4ccf520e4ca5033ad9510c28389a1c373884da454754a476`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:16 GMT
ADD file:cbc540158e77b85113e3a0e0ed1e202046cf293cdb8d7cd890b04883493dbf35 in / 
# Wed, 14 Feb 2024 01:47:16 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81badc5f380f1ca21f6c430303f4107b9b5e0af27c59e3725bf731915b457fc8`  
		Last Modified: Wed, 14 Feb 2024 01:49:17 GMT  
		Size: 51.3 MB (51325575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f943f48ed43ed865465947885a23f9ca429300b7943b988ed9b49fa7a174662b`  
		Last Modified: Sat, 17 Feb 2024 00:53:48 GMT  
		Size: 15.0 MB (15005859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac5e3cca0f313dfd16002062e9f1a6fd48c66b5f3a8cfa5f8ddeb1fa53d9ffa`  
		Last Modified: Sat, 17 Feb 2024 00:53:50 GMT  
		Size: 202.8 MB (202768181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c9363795f2671b5aaff1b0ea4bb48c49ab47af88d6b84001bfb1657f0c0d0abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b56c12f0efcf9d6b68075ad59d3e304d3871950b10aadf97490c186bbce1974`

```dockerfile
```

-	Layers:
	-	`sha256:ad65a5868101d1ec11d717facb00ff721dcb10744b12ec2cc5aa9f38295c96c4`  
		Last Modified: Sat, 17 Feb 2024 00:53:47 GMT  
		Size: 2.3 MB (2269266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7570de2503bee0e1cbe45e3a5601d8244cff54a8ba9149011327eabac6a65235`  
		Last Modified: Sat, 17 Feb 2024 00:53:47 GMT  
		Size: 18.0 KB (18025 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d09f2e82055cbdcb4a32d601d15d28149719715ccab05d9283564ea64a7f120d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266588997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83d359d5012e197484fbbdfcd46d9fae1cad90b20681516ff2307858ab0ae4d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b1d3eb6a012567065354e86eb0bac67a32e425e65bc6fe8b5cd84b95a0643`  
		Last Modified: Wed, 14 Feb 2024 11:04:46 GMT  
		Size: 15.7 MB (15691290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30549fa3ddde3809fd2069181de3010bb5522bfb570478076e9722d4e5bc0dad`  
		Last Modified: Sun, 18 Feb 2024 05:21:03 GMT  
		Size: 200.8 MB (200824793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ff63298e889a1ade26cd0275dcab4530f68b134defb150468f729c84a12aec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5543d675ca97f2e4c5704f161bc9cdb6f31518f39de726ef563455b852683d10`

```dockerfile
```

-	Layers:
	-	`sha256:6ba93f9c4f99d00bdc70361b302322c9d91be3fa41e5ff041437feb9647cc49d`  
		Last Modified: Sun, 18 Feb 2024 05:20:58 GMT  
		Size: 2.3 MB (2268682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9fc41f90e6b60830e8d63263312e76253a2350e659d9f49678aa6331619551`  
		Last Modified: Sun, 18 Feb 2024 05:20:58 GMT  
		Size: 17.9 KB (17883 bytes)  
		MIME: application/vnd.in-toto+json
