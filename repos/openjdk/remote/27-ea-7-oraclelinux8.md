## `openjdk:27-ea-7-oraclelinux8`

```console
$ docker pull openjdk@sha256:dc8a4dd3bfe5f63c854fa885ee0ff149b41815b6db9e7295e0e853be120ecf4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-7-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:8851457c738ef5bca19c70b8dfae7645db48ba327ae8f64d2a1d72d1c6e873c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295147206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29470269ac05f5349778f65c372a1cd8b7b24da628d3841c1169fa39b489757`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 17:47:46 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 17:47:46 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 17:53:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 17:53:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Thu, 05 Feb 2026 17:53:38 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:53:38 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 17:53:38 GMT
ENV JAVA_VERSION=27-ea+7
# Thu, 05 Feb 2026 17:53:38 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 05 Feb 2026 17:53:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:491a81275e9334940c80f680a1adb0db6fd283efcb818f679954c68fba010df0`  
		Last Modified: Thu, 05 Feb 2026 17:47:57 GMT  
		Size: 51.5 MB (51465258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df0c1e75b214b5fadd84fc8b041e12a391eab94b66ab2a0bf054652940f9aa`  
		Last Modified: Thu, 05 Feb 2026 17:53:58 GMT  
		Size: 15.0 MB (14991491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285660fdc7f02c4de2a98ab19b33b381df11a0690b18d3cabbebbf874737b0d`  
		Last Modified: Thu, 05 Feb 2026 17:54:03 GMT  
		Size: 228.7 MB (228690457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:226b660ef12dcae74f2d24fcf8c4ea398c22804bcf23f326633e4292e1df90bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69fc8592dafca6d8caf70edf981a4559e72c59dc3a3830958d8eac9070994ae`

```dockerfile
```

-	Layers:
	-	`sha256:04feca048ccd0be996e90ced63d34e2a555530d75732d758969998f6a911a79c`  
		Last Modified: Thu, 05 Feb 2026 17:53:57 GMT  
		Size: 2.4 MB (2448060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134af340d6d3ae2430c88d704befab8fcbfe31c0b74fe97ac7fcd9c229b4e2f3`  
		Last Modified: Thu, 05 Feb 2026 17:53:57 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-7-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1ddb0f840f751223c99101f007ced4262c83bbc47920f532560dc379637c3614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292535914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204c464153715776bd599b725412e899af2ba1fe38f2d8ba34eabaf64020c611`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 17:49:16 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 17:49:16 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 17:55:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 17:55:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Thu, 05 Feb 2026 17:55:58 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:55:58 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 17:55:58 GMT
ENV JAVA_VERSION=27-ea+7
# Thu, 05 Feb 2026 17:55:58 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 05 Feb 2026 17:55:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13fbaff937e13295e4b8a7721c793f2982cdaf237b88f7bec2c123e9744840e6`  
		Last Modified: Thu, 05 Feb 2026 17:49:27 GMT  
		Size: 50.2 MB (50197611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d1b47b7b1e4c3b98b76c9f66c4df37a7c4cbc1d49b1144bc476f80efc9bd6e`  
		Last Modified: Thu, 05 Feb 2026 17:56:19 GMT  
		Size: 15.7 MB (15695117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1751518d99093de0be445df8e80335136b4e8915d77380d4318f756c8573f618`  
		Last Modified: Thu, 05 Feb 2026 17:56:23 GMT  
		Size: 226.6 MB (226643186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:3e29305767e2f10b15fe2d43de088aa771e2afb740777347d3e3a60f432c97be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180fe929168c527a75fbadffdfb23a419b689ce3104a4e428a26480c4f378f48`

```dockerfile
```

-	Layers:
	-	`sha256:4ed8f31381e0772d17a73d7636abbb8d9e5e6f30616ab4f5e753824a82229503`  
		Last Modified: Thu, 05 Feb 2026 17:56:18 GMT  
		Size: 2.4 MB (2446870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35363103158d1d570029440267ebf3017c9fa7e500ccec19e058c3aa81b9e277`  
		Last Modified: Thu, 05 Feb 2026 17:56:18 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
