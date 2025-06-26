## `openjdk:25-ea-28-oracle`

```console
$ docker pull openjdk@sha256:5f54a501b300befaaf0d2bcc54ff266c0f226c169f052e76014a27cf513d377d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-28-oracle` - linux; amd64

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

### `openjdk:25-ea-28-oracle` - unknown; unknown

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

### `openjdk:25-ea-28-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5a2015d5b8f7b366d95e6575553993f081e5e441c520bdadbe0d67e5b3556225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307356913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c7d0c744635b4a0affdcd626af5baa3209c959f9aaa923196d5a44e1f604a0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Jun 2025 18:48:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:8651adb19772f22f50f38bb61855702b5099b0a0045fea8c9db8dcc1cadfea34`  
		Last Modified: Thu, 26 Jun 2025 05:13:18 GMT  
		Size: 48.1 MB (48087180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf0ee1c604fdbae17917604a097f1f42ae8abcc22cd62c1260386266d1d6ac8`  
		Last Modified: Thu, 26 Jun 2025 04:43:33 GMT  
		Size: 38.5 MB (38495135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a23e2b4ae8b3015d01e481c00e1dd8fb9734cba533b39df9609183b6c15bf12`  
		Last Modified: Thu, 26 Jun 2025 06:52:49 GMT  
		Size: 220.8 MB (220774598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-28-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9489a272f4c4669ec1163a6621102f1e61896e0ff590e9b78df1fea9071eab0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f09ecdced49362da516f10e8a9ecf40440403d38ee1c72345a19051b08237a`

```dockerfile
```

-	Layers:
	-	`sha256:258c99a4230ac162ca8b4090ef005eb07895649d67cb9fb18ea194ee3aebd776`  
		Last Modified: Thu, 26 Jun 2025 06:23:20 GMT  
		Size: 3.6 MB (3639070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336e5b31efda4e8e4e5dfadb1141598601e0359c6cdad92fa23bd45fe04d38cb`  
		Last Modified: Thu, 26 Jun 2025 06:23:21 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
