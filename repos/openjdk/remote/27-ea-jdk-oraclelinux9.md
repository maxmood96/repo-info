## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:21758153b283864ad4e1e44d952dde86a869c0cdbce2ec6328e28b89c6e2f4d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:90588f87f9450e9513aa5961b67cf5bd951a1048897c62666dd718f99bc83271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314220022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61c121a858485b03529fe382ea58cbbdb1daed5b778445848aca4ff9e080820`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:12:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:12:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 12 May 2026 19:12:57 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 19:12:57 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 19:12:57 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 19:12:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 May 2026 19:12:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1034dd9627f42df7d8f74034a47e8812e0e6383b5219908f3e67e2fa8de790c5`  
		Last Modified: Tue, 12 May 2026 19:13:21 GMT  
		Size: 38.3 MB (38268071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73489ff28e40b231f56a0af64ba37a7b94cd62127ffe4ec5d41d2732b5c3d1bb`  
		Last Modified: Tue, 12 May 2026 19:13:28 GMT  
		Size: 228.6 MB (228642378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:bc855995e2f9a4be339936d3198e432efa1b624969f610a1cf86f6cff7169e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a86ff8218670916061f95dbd5dba59c6df7e075833091837ac96169b3eab99a`

```dockerfile
```

-	Layers:
	-	`sha256:1d51af8dc4ff0506da2c8903903e5a511f0878087f971ebd33c530492b0ecc12`  
		Last Modified: Tue, 12 May 2026 19:13:20 GMT  
		Size: 3.7 MB (3651703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207019ee04016989dba53e0657f6a23a56ae7be03a33a3d26e40b6e283d8560a`  
		Last Modified: Tue, 12 May 2026 19:13:19 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c765cb46afa7bcc0451199ddcf9bb17464c3cd23142d88479b7dd4d7a4227486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.2 MB (311160052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc675928bb0e99a0b574fb7fe2214cc09da76885f7f4b53b8a4ba2bd1e74e0db`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:12:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:13:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 12 May 2026 19:13:01 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 19:13:01 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 19:13:01 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 19:13:01 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 May 2026 19:13:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01b44ac26754c7f2c6ddaef4ecc77c21b9d991b4480a6f8ecae04b93fd0a56`  
		Last Modified: Tue, 12 May 2026 19:13:24 GMT  
		Size: 38.7 MB (38663522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b17aac90407a4681b6e055dc68fe722f67d0f3a0a4cc247554fad9b17e98b79`  
		Last Modified: Tue, 12 May 2026 19:13:30 GMT  
		Size: 226.6 MB (226597440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:bba19ddcd3a6f1a53f66b4677a08f7c9a78378f114aed587b1138f78a6c20285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3664759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67342da613eaa17fb6c8e58fd6ae1306de6de185bfd490f554288d00a0f45a25`

```dockerfile
```

-	Layers:
	-	`sha256:e9bbef01a66281f01a7973b2270d87ea3731aa5aa7b7b93c53a8f005adcaab6f`  
		Last Modified: Tue, 12 May 2026 19:13:23 GMT  
		Size: 3.6 MB (3649297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a2993641d2ed2ebe63c6a8894f935d5b92e0e6108f8b229290cf07f4c0666b0`  
		Last Modified: Tue, 12 May 2026 19:13:23 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
