## `openjdk:25-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:9a580d4bf74a90d946a1baf570fed58efd1e55caa2d718f0035c0477024ef23d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:30a133d2d99ee3cc520bca3c063ebd29275c4371903de7205a7f98af5ee6c8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299381719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1484316d4db0258e8e19a2bf9d75add2916bc875d49d5521d3c9e0b506047f93`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Mar 2025 18:48:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
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
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9120072ebb306ef7c18220aa546197aa4d2fc298fc802fbb31dcfb8532b29b9`  
		Last Modified: Tue, 01 Apr 2025 01:08:16 GMT  
		Size: 38.1 MB (38108841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02203f9de33e1c9b6e369793c05c07044cf741b10032448b47590c1d985c375e`  
		Last Modified: Tue, 01 Apr 2025 01:08:19 GMT  
		Size: 212.2 MB (212181668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c50069fc7228744eace4dd71d28b690ae93bd89b1f03bab5f62fa3a5c49bc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3644246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6c683c771cd7c581321a6d34ae2571406854d29d31684ec7dde99a50199a9b`

```dockerfile
```

-	Layers:
	-	`sha256:db153ab208371a29982fd325c3abf02a98a79705f01a94a6e35eb395d1875b6d`  
		Last Modified: Tue, 01 Apr 2025 01:08:16 GMT  
		Size: 3.6 MB (3624500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0bc3e05334afb2081cf3d90ea799f313e80122e7ed4e36cb1c36065b87d2e4f`  
		Last Modified: Tue, 01 Apr 2025 01:08:16 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fb5c84e8422471b0a286fc694d5fb077ec080b98280ae233f73851cece8697d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296243928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6492479000682f9ce3972d01be2baa36bab411008a34fac17e137df256dbcfe`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Mar 2025 18:48:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc73a32668bc167dbd00ff7118bdb7d58568584dac2f5c61e9057497c36e654b`  
		Last Modified: Tue, 01 Apr 2025 01:13:12 GMT  
		Size: 38.5 MB (38500679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3901822fe189d9992fdb8c1e49850ef36fe57efef49e5f439af891e15f1c0a8e`  
		Last Modified: Tue, 01 Apr 2025 01:13:17 GMT  
		Size: 210.1 MB (210068426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:54338ad3ac87e998a206c4684e3450893b3e87ecbdd108df07943a1c9290c7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214e8b74b0dfe6ec84096bb1ade4c30d734d36eb0d8bf8f0ae27edf673045071`

```dockerfile
```

-	Layers:
	-	`sha256:be7aa3e2f51af1b561770ed6538259c2b4309cfd7c2b79360cdcbd0391cdf008`  
		Last Modified: Tue, 01 Apr 2025 01:13:11 GMT  
		Size: 3.6 MB (3622262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b250bc2792dccb8e6415b25ddd223621c0dc92d15a57f9c951741a76ca37198`  
		Last Modified: Tue, 01 Apr 2025 01:13:11 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
