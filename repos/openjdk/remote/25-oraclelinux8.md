## `openjdk:25-oraclelinux8`

```console
$ docker pull openjdk@sha256:dc123597af6c5d3491699c5006db264af2c17325509052f280b3b7f955ce8865
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:8d4aafbf520f544baceea073ac7f22398744da498ce21dc972309f1f5599e4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278926085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b400e1e3b054915ad1cd81c784aecfa035dc8ef25c844c06b3f4a8bd9821b0fa`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Mar 2025 18:48:13 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:079caf22b235d19accaab46f0177ccda24bfe8b1c7622e0cd0cfa34e087ba3ad`  
		Last Modified: Tue, 01 Apr 2025 17:12:53 GMT  
		Size: 51.3 MB (51287468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e68cd5ed66e7641cd808dba2a7e0476fe8964d71ca52228cef6a50a101fcb1`  
		Last Modified: Tue, 01 Apr 2025 17:17:46 GMT  
		Size: 15.0 MB (14987154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdb5f039352bba8e408079f949535a5c4ff2a620e4a9636ba7b35412feac8f4`  
		Last Modified: Tue, 01 Apr 2025 17:17:49 GMT  
		Size: 212.7 MB (212651463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6af96f8550689d58b5b6aeb8db7f94ad48a3d4edde54c5e4ce3f02afbc2d90d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09ab2781c7c9029e4f6ffde4336b70d15b00054ca55bef2ef5a136047d0c297`

```dockerfile
```

-	Layers:
	-	`sha256:04d6a6d02717a3fccd0a23a66cdb3599a2ee157ef7845b36b562555d9799aff5`  
		Last Modified: Tue, 01 Apr 2025 17:17:46 GMT  
		Size: 2.4 MB (2442869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf592cdbe49a460896f18ee3edfd623373ccf8972c0a970aa267c110cad6082b`  
		Last Modified: Tue, 01 Apr 2025 17:17:46 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:42b4b76d7c689f8398ab65b4be0d0a07bc93c2b1cb1b139c5ba84911036a840d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276216564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e858f89b8aa35f7f4272e3a34f8e5a3c023d4ad1789b0c9952b4cd12bf3f0c0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Mar 2025 17:20:57 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Mar 2025 17:20:57 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f8eb825c1fc22ded5eda8a11c91fd13cd2b63722a0fdbe5ed89339ba10aabad`  
		Last Modified: Fri, 14 Mar 2025 21:52:22 GMT  
		Size: 50.0 MB (49989226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d2d63d00da99812eb8285d347cd8a68c6913a3b4f406a756d3804e277dc4d6`  
		Last Modified: Fri, 21 Mar 2025 17:24:29 GMT  
		Size: 15.7 MB (15683223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c796d313a2aa05c5058d5f27bd4e2043ac38b69e7fa4a2ebd68b30cdecbb9dd3`  
		Last Modified: Thu, 27 Mar 2025 20:46:14 GMT  
		Size: 210.5 MB (210544115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:261c11b1e09b8a2216e7ad7185f502bf956097a90831f84e8742106cf3c90c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3433f5c1cfebb2993f0aadb5122d09e2379d7e65e7968f36c2b75566b802d43c`

```dockerfile
```

-	Layers:
	-	`sha256:da4aaa3779851072fe9fc982b89c51c64ee0b7d429f8b648ef77c7ddc0d02824`  
		Last Modified: Thu, 27 Mar 2025 20:46:09 GMT  
		Size: 2.4 MB (2439813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d138d2bd6e6cf711b81afb1e3eaa32a3f5b27bced42abd1985945081a70f2fed`  
		Last Modified: Thu, 27 Mar 2025 20:46:09 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
