## `openjdk:25-ea-oracle`

```console
$ docker pull openjdk@sha256:9c645de7ddfd95705b75407d29338a5d44c393e1bc5c06a4040a4a0d6e3dc2c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:237163dddb0d1e071539a5d75f421ee1794248f26e9e9765dd7448187873b669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310588310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7526537d02538bc7ccbb42aa651bbf6616b959b4e9a1ebfb9ef101942133a750`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Jun 2025 18:48:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 20 Jun 2025 18:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_VERSION=25-ea+28
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='ddd476f5dc6e80fc93f06ba240cf3537fd8aed344823abfd64c1cfe470f441b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfbc99aedd5015a5ab41d74f53972f7cb6616032c983216add8cf2de21a1fa5b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7914bd932e7c4d5b34a551c32127deab484f059a8ee68fc9a74db0afcab559fc`  
		Last Modified: Thu, 26 Jun 2025 00:09:23 GMT  
		Size: 38.1 MB (38092132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0a6d0100a73bca2b0883910209c4c216e5e8cc5403b4e3871fb08232a72db1`  
		Last Modified: Thu, 26 Jun 2025 03:32:06 GMT  
		Size: 223.0 MB (222995516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:641fe90035e52369d0fa34842fe207b4fd55656d2f0b9013625e6da6d4ee77ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed42e17ee6bb3d1784f9d8fdc03dcc55621dc80e41850cfe31da94d7b6282843`

```dockerfile
```

-	Layers:
	-	`sha256:b570a4632dfaa31a446494e9d2a9afe77b43f9e7de448debf755d9f1a298217c`  
		Last Modified: Thu, 26 Jun 2025 03:23:19 GMT  
		Size: 3.6 MB (3641308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:087e74c16d3afe04aa24be234ad60edeb1f6f6f5e087a41781fd887ff5021c12`  
		Last Modified: Thu, 26 Jun 2025 03:23:20 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:51d4f4e884332d99b7caaca8e6682ead823449a960a7c6bbfcc35b7e52f8f8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287185943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda11268dd8d66c7fc09f3974cbbf1b36810861cf86a67a0edeeec9b16a9608a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:37:07 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:37:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 20 Jun 2025 18:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_VERSION=25-ea+28
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='ddd476f5dc6e80fc93f06ba240cf3537fd8aed344823abfd64c1cfe470f441b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfbc99aedd5015a5ab41d74f53972f7cb6616032c983216add8cf2de21a1fa5b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7e489c978e38b5afa5d393fea94c54ad3525e6f544c411be6e80f47ef76d0a`  
		Last Modified: Thu, 12 Jun 2025 06:41:39 GMT  
		Size: 18.3 MB (18321513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da5824aa2245ea218a76f9b51fb7c4b4b3002f26edadcfd4f2209f3d76c9a7b`  
		Last Modified: Sat, 21 Jun 2025 04:20:08 GMT  
		Size: 220.8 MB (220774635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1a95b99c787298c5a84ac819eb2a79bb5ef18fcbab386baca2ac8695f363721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bf1d8f8c70d2b104e9a9d67d5e3e4cc108167e713ee4662dd5ed614bc7e620`

```dockerfile
```

-	Layers:
	-	`sha256:cbca62b4f8e06b125fa28091c3bcd51275daef81709b0c0c3e74551904cd3d1e`  
		Last Modified: Sat, 21 Jun 2025 03:23:31 GMT  
		Size: 2.6 MB (2602115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac0e9f8086fa09721cce55c3a04cdbd2d041bc49b303dae36bc57eb9b7d2341`  
		Last Modified: Sat, 21 Jun 2025 03:23:32 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
