## `openjdk:27-ea-21-oraclelinux10`

```console
$ docker pull openjdk@sha256:6d8ad8058f441a51451a4e1553d3f4d10a24c79e5aacd7ab949f50b320b5b207
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-21-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:11561089adb4700256315df7e4e6e6f365e9666f39dbac747a2af5e8dd09333f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309405477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccae5fd411591f17c8e2f1ebde784d39c1b5982dc4115b9cbd5989b64023dbf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 22:03:00 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:03:00 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 23:50:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 11 May 2026 23:50:35 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:50:35 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:50:35 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:50:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec2c75dc3bcdc3cbe3d81597cf6bc4be9a4be0da377a5e9e20a8ca4ce05ceafe`  
		Last Modified: Mon, 04 May 2026 22:03:10 GMT  
		Size: 43.1 MB (43077903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449cd9a13c6daeb87022511d51fd07307bfd5e95eafe644f45f9624061155ef2`  
		Last Modified: Mon, 11 May 2026 23:50:58 GMT  
		Size: 37.7 MB (37684978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48049791d36ddac6f1771483343085692b1db9a2daa2e9c784a32e096c0d7f80`  
		Last Modified: Mon, 11 May 2026 23:51:04 GMT  
		Size: 228.6 MB (228642596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-21-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:3dee10c7df760cab70e3a436316ad21e5c46ef1bee5736bfcfb746152aa6cc19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478028f9ae3ab6a16832aceb8452ef6d8acf9f30b48e0fc22d83c91dbc87e3df`

```dockerfile
```

-	Layers:
	-	`sha256:80f77a15b0f19f186e21963f0d06477e4996e54761f4d7ad0f84f615f0a9a8a4`  
		Last Modified: Mon, 11 May 2026 23:50:57 GMT  
		Size: 2.4 MB (2367791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303354225c37a414314363f264a40099c5159f3feea560bac021082c25978fb0`  
		Last Modified: Mon, 11 May 2026 23:50:56 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-21-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4fb63d168604b5dc318e171495c7406122cc917ca0de6ba2521dbcb03243036b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305769937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354f9d7a060ad68773f499708083545d658a22ac72b5e8270b979c2c6c578089`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 21:01:45 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:45 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 23:51:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 11 May 2026 23:51:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 11 May 2026 23:51:32 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:51:32 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:51:32 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:51:32 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:51:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5668b0574ccb4784e2840d685216839b685818991f45396bc2df53f234772cca`  
		Last Modified: Mon, 04 May 2026 21:01:55 GMT  
		Size: 41.5 MB (41471545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720c3513738f59a4f90ee3b272548b71698af45e40a844eabbd0daf84a96a9b`  
		Last Modified: Mon, 11 May 2026 23:51:55 GMT  
		Size: 37.7 MB (37701048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4e925a0c733c920b616f6276c25604b0827e1db1b2ed2298c944834dcf19e2`  
		Last Modified: Mon, 11 May 2026 23:51:59 GMT  
		Size: 226.6 MB (226597344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-21-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:f2d17cae6cbfaa9e5df47af676f967220a0421bf8414419e0ffd4e9b5a0b01c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ce9479edb1777ec388a8f15cae6bc446740d36430664523cb13514dd04aec6`

```dockerfile
```

-	Layers:
	-	`sha256:587d6cf4002ea050b9af4a43ffae95d0aca7425eb53cdf8cc01edaf90a69f1fa`  
		Last Modified: Mon, 11 May 2026 23:51:54 GMT  
		Size: 2.4 MB (2367319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ab047d27beb946163e131f8375b835aadab0182d5772c20c2829b60e47bcb8`  
		Last Modified: Mon, 11 May 2026 23:51:53 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
