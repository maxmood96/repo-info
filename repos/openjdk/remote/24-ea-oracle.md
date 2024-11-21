## `openjdk:24-ea-oracle`

```console
$ docker pull openjdk@sha256:95f285a61a8c09d535aefcfae503679ddb11dd275f889c456ac9bb4f8f0818e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:f8a15c2a3677e1b9d61c52cd26e0befe2ee9e116fded6559369bdb0b4bce4a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (319965291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1b33deef2113c0d461d5fe924b37aff09c0c9d3d7e9e8257a2af4784064c74`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 01:48:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de55b856695104a1e3b4f7303ac9340c9c03666ad0b94bc957975fd559f039df`  
		Last Modified: Wed, 20 Nov 2024 23:21:52 GMT  
		Size: 49.1 MB (49099176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca87ba9dca4341a2fed277d7ac6a1357c39032b94cb137304ddcfd4ea05fbd2`  
		Last Modified: Thu, 21 Nov 2024 01:22:21 GMT  
		Size: 48.8 MB (48764043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24c15910d82a988c067a18b4ce4a096d816e53e70efa4a1f9047e609c923540`  
		Last Modified: Thu, 21 Nov 2024 01:22:26 GMT  
		Size: 222.1 MB (222102072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b34d297978612f5db12de7636b14cc6934c042c1da93d7b07f4c2627645c53f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bd4b659c7ced5aeceaa5dab53c9956cc7df118a1d46f355cb1ddc1d0aa2338`

```dockerfile
```

-	Layers:
	-	`sha256:48265ef9c4da65b50bda3602a7b6bced61d5ed1f0eadd0ed94129557065f5fde`  
		Last Modified: Thu, 21 Nov 2024 01:22:20 GMT  
		Size: 4.9 MB (4913833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd42188eb1f0f0bf751d083718bff34299108ec85f3e8d85f0d52544e9521fed`  
		Last Modified: Thu, 21 Nov 2024 01:22:20 GMT  
		Size: 19.7 KB (19744 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8d0f9949dfe1d1ede0af6b2119c3b4e1ff926c09da036c5ce5481f5c333c417c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316907702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9302799bd33f11e1d0ffbc1f894c269b869c44b0354b7a2c9a95380d830b4e4e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 01:48:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a93c535b15275685f3fe8d4b18a2d8a13ff61d328c77a9e6c83cfeee99db3b43`  
		Last Modified: Wed, 20 Nov 2024 23:22:34 GMT  
		Size: 47.7 MB (47668111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5f8de4f2d9969760f7305bcb7e581f11d06e50c55da9047cbe18516bcc67a0`  
		Last Modified: Thu, 21 Nov 2024 00:29:59 GMT  
		Size: 49.2 MB (49187501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2320b77d4327274dcf0ffc81e0a17eda24a9d1ad2da368715e259238b3785185`  
		Last Modified: Thu, 21 Nov 2024 00:30:03 GMT  
		Size: 220.1 MB (220052090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:31b9e167b4742bddebfb94e776b5cd00abd6851a8d0a845bd89d5ef271bc873d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32d32995686c25256292ce99e4a683663a84dabfa5a0b58e713fdac13c8ef81`

```dockerfile
```

-	Layers:
	-	`sha256:923570b29d671f57035e283893d41084b37160a6419b0e154909388efd58f8cf`  
		Last Modified: Thu, 21 Nov 2024 00:29:58 GMT  
		Size: 4.9 MB (4911591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3906beef4db84530586ed8dbb8977dc0f94df8eadb7715e5fc292f76e156795`  
		Last Modified: Thu, 21 Nov 2024 00:29:57 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
