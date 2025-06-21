## `openjdk:25-ea-28-jdk-oracle`

```console
$ docker pull openjdk@sha256:76eff3b9ffcc9d0a4ea2a724f357f898b105a2e5d955118c60b068d764b2597e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-28-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ac76d38f4cabbaec5f817d646a5df8defe81d8b0b53071a1009a5339b2d71bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310577591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cab4285b16109d4394811ec0d7e3378359b43a0f90428d69220b95af9556e2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:36:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:36:51 GMT
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
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07c3de0bdc2a1cde59e760a2026238f682a2e6d454def426a704400c2fc946c`  
		Last Modified: Sat, 21 Jun 2025 03:24:35 GMT  
		Size: 38.1 MB (38081270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bc510c2b29052cf14216d4f857b334692702fc649d29a25a106dcf5de84107`  
		Last Modified: Sat, 21 Jun 2025 03:24:45 GMT  
		Size: 223.0 MB (222995424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-28-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:ac023174a29433fd364880ef04c079a10a7836df5bf679b89c650159aad59ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb317ee1d737e60aa9f47bd96c95b41e2563bf87474fdee8859b2a018e4cee5`

```dockerfile
```

-	Layers:
	-	`sha256:d4ced223dfda25db8296cba24fd53563478e656e9f4b5333213cdba6d202c4fc`  
		Last Modified: Sat, 21 Jun 2025 03:23:26 GMT  
		Size: 3.6 MB (3641236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27022af808b5742457269f418aaa2f2a9591cea87857998bc9935ec9e4ed6e5`  
		Last Modified: Sat, 21 Jun 2025 03:23:27 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-28-jdk-oracle` - linux; arm64 variant v8

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

### `openjdk:25-ea-28-jdk-oracle` - unknown; unknown

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
