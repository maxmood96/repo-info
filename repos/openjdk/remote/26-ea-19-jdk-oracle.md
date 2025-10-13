## `openjdk:26-ea-19-jdk-oracle`

```console
$ docker pull openjdk@sha256:6bdf9c522dfc790e09d616ae58b8e9ff98243ebbba3b4d6d12e3e755cafd0d48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-19-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a836fd2f61a5c61be8cb6fa05b386ab9d682fe6e39cc7390290d331405e66754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313276012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936ed279b76256479bc4ac2a1bc764020603cca02469f6ddc42d5d9449015c57`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93c8878a2cdfd2dc50032c3572c9b627079c5632261fd3256ee3992dc0e12b6`  
		Last Modified: Mon, 13 Oct 2025 21:03:29 GMT  
		Size: 38.1 MB (38082794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb02e6489f4563d93b520919c701424762c708ea1d5d6ad0e6f8ed21d92a74c`  
		Last Modified: Mon, 13 Oct 2025 21:44:01 GMT  
		Size: 225.7 MB (225696222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-19-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d66e37dac03b419ecec68d0d407fcfc2f1693cb661b122f24ac3e2e733ab52fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b787fc8b4860bc71972d0fbf8494979521f8ff7a7a7f769e2767adaf4eb66610`

```dockerfile
```

-	Layers:
	-	`sha256:3f33e79370ec6c6ac28ccf77a860af7b9c07136e99688903dde1a82a23101dbb`  
		Last Modified: Mon, 13 Oct 2025 21:23:26 GMT  
		Size: 3.6 MB (3640737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf64b528cd98eb4959c88ada35227ace8388eb3967fe3f245baf9bf24d415163`  
		Last Modified: Mon, 13 Oct 2025 21:23:27 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-19-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:518992b4523d828058fae037c21b2f4a2b0f448fded31cf05965c024c855c949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310131876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b4fd0300a1d7fa5bb4e3da8d35551153745a8f31d3fab7e81cdcb145d50d74`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dde7f62f08c4f419f5b4d9cd6e8ca61653d876c53d501862e61f852e10141b`  
		Last Modified: Mon, 13 Oct 2025 18:20:13 GMT  
		Size: 38.5 MB (38490273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21451a66ce259cf7b8828e9dceb273999673d5d91342ac8c2fd51c435bdb3031`  
		Last Modified: Mon, 13 Oct 2025 18:18:18 GMT  
		Size: 223.6 MB (223553306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-19-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a05b68b68de53980544b431212583f470fc021f423a57939446dc9db862d4b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87be79be9029cb84fed66f4dd49199a56b5ef92605d76c0b2c06c480a15a3fb`

```dockerfile
```

-	Layers:
	-	`sha256:1133a1bfbbf5192f569fd287b981ea74c90ab2b4550b126572fe941d862eb8f1`  
		Last Modified: Mon, 13 Oct 2025 21:23:31 GMT  
		Size: 3.6 MB (3638499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f709a2b22ef7542e335a7be86690575871a59b7dd9183d0d3e28235954d31e36`  
		Last Modified: Mon, 13 Oct 2025 21:23:32 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
