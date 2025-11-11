## `openjdk:26-ea-23-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:7f5ec43201910f96fb46ecde59f75d6bd9c12addea164287e14f5b53a984750e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-23-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:01e6c5849a83abe778fafcdc7489f26c4e76b3a07df27ed47dc3d68c9d8cb698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313427543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e32f9b52ce76941ac99a5113c29ba966a6b31ff39fc6819896548bfb7b750e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:53:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 10 Nov 2025 19:53:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 10 Nov 2025 19:53:19 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:19 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:19 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60640e79d279fe0316db1af5ebfd70a728168431645d79005f89dc619ff586f6`  
		Last Modified: Mon, 10 Nov 2025 19:53:57 GMT  
		Size: 38.1 MB (38086182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55c0233a4c209f46c0811ec2c212e0ebd7989ad6be913d650e50c33e60bfaf1`  
		Last Modified: Mon, 10 Nov 2025 22:24:07 GMT  
		Size: 225.8 MB (225844856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-23-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef67699b28a3871d42d7a3a8d21c09f601eb2995a3cbb1c3c0b3be7c06d458f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3654221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266facdad2ff0246c17b7056c971da75cae29ff11790510171d45bb91bc20aa4`

```dockerfile
```

-	Layers:
	-	`sha256:419624f5b92bf09352b7204552253c2d61602336e4b63b2045910983d5d638c4`  
		Last Modified: Mon, 10 Nov 2025 22:23:26 GMT  
		Size: 3.6 MB (3636382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a379d3ffc819d5ee8fe5ea374f132541fc933e3175457a6a18f7708528524fa6`  
		Last Modified: Mon, 10 Nov 2025 22:23:27 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-23-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ea1de56d016f68bc6fccafd1d34ba50c615eb82760c275ab524041a26586b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310278297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecbf554100a394499239558871dcc1405cf07b1de9c7019ac36b9800df3fde3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:52:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 10 Nov 2025 19:53:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 10 Nov 2025 19:53:09 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:09 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:09 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01aa7bc1ecdda76fbb99dcf68777bd5b2432a2b3113967e5409b9df0a879716`  
		Last Modified: Mon, 10 Nov 2025 19:53:48 GMT  
		Size: 38.5 MB (38490872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d920c579ae991e390794fbf170533c9a564ab60b59e98a7e2324d131fd70493`  
		Last Modified: Mon, 10 Nov 2025 22:50:20 GMT  
		Size: 223.7 MB (223700524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-23-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:a42928ac6c5437e94e237ed2cfc13562824527150a4671c33b6fe9b15ea428ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3652126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28411bbc7c2b21517a858b867e9c3e534dfe8e5b4bb97989bbfc60fcfdd6d12e`

```dockerfile
```

-	Layers:
	-	`sha256:1b16a1581afa6a97d827bb0b24f60984396cf55f6fbc0136e68c62e0465bbaab`  
		Last Modified: Mon, 10 Nov 2025 22:23:31 GMT  
		Size: 3.6 MB (3634072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d1504a3c738c72dc5020ebc62f50ee33e0d547942f43970d33f746d2f8f0a5`  
		Last Modified: Mon, 10 Nov 2025 22:23:31 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
