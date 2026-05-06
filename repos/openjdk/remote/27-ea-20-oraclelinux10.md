## `openjdk:27-ea-20-oraclelinux10`

```console
$ docker pull openjdk@sha256:209d4c782c0d076430419cc79147cbe25ac7f50ad6aa796ece0d236f9d678a65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-20-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:8863e5ad04933d7a13d8bfe36b6203bb779dce1aaad7ccf4868c136821cf4056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309230477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01deb3d558152bf59e378348745a7cecdef8a6fcfbddfca6296f51915f039aa7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 22:03:00 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:03:00 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:02:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:02:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 05 May 2026 23:02:51 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:02:51 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:02:51 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:02:51 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:02:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec2c75dc3bcdc3cbe3d81597cf6bc4be9a4be0da377a5e9e20a8ca4ce05ceafe`  
		Last Modified: Mon, 04 May 2026 22:03:10 GMT  
		Size: 43.1 MB (43077903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d1b9a15d22b55f24dd92483a1996076e044e82e19cbfc38420e330fd7a386`  
		Last Modified: Tue, 05 May 2026 23:03:14 GMT  
		Size: 37.7 MB (37678657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70f23a14e1fbc561de0c7a06a49a53be33edcb28d39665d6eee23db201555cc`  
		Last Modified: Tue, 05 May 2026 23:03:18 GMT  
		Size: 228.5 MB (228473917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-20-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:c7e91b3fdb96090e2dba2ca985f481198cd3af90216fbced377b02fa2ed2a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2cbc49240d0a9566c9c0fed2baf580deda0ea4f699a9435999e2922956b5d1`

```dockerfile
```

-	Layers:
	-	`sha256:134827b1676a3149c287cb6b0d7dcaaf531b74b5b717b1d8d59ffe38f36e4284`  
		Last Modified: Tue, 05 May 2026 23:03:12 GMT  
		Size: 2.4 MB (2367759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d7efcf2febd708f8efba9a7c6e09305e4296197f30ad05c205b079214e9af3`  
		Last Modified: Tue, 05 May 2026 23:03:12 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-20-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ae8ffcdf52fadf5c0ab03d2c1f25b6f5f5eade953cec852ead618645cad36f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305604557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2032e8ed0b049618686868a1528d6bb7b838b4e17cac7ce4db715b7c3d2a7d73`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 21:01:45 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:45 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:02:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:02:59 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 05 May 2026 23:02:59 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:02:59 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:02:59 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:02:59 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:02:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5668b0574ccb4784e2840d685216839b685818991f45396bc2df53f234772cca`  
		Last Modified: Mon, 04 May 2026 21:01:55 GMT  
		Size: 41.5 MB (41471545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a87701ef34527a61b398666616cc8e6b4e19212bb38abc1100606df4ad0dd`  
		Last Modified: Tue, 05 May 2026 23:03:21 GMT  
		Size: 37.7 MB (37698072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccffa9d312bd28f643d08f668768b9628ac18318062afcb26463e6c0096c7e64`  
		Last Modified: Tue, 05 May 2026 23:03:26 GMT  
		Size: 226.4 MB (226434940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-20-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:e8df939a8f3c29b27c89c334ecfaf51cd326c48c049fcc7a3aeab4deeadc7c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f6c3346b444fd90e1d85a7b6c41a5a6796fa9c83bc0cc312a9a892431ffc6c`

```dockerfile
```

-	Layers:
	-	`sha256:53aaebb0b18da07ac384cf36165ed1911c79b89a9cdc791826c136aa2cc61770`  
		Last Modified: Tue, 05 May 2026 23:03:20 GMT  
		Size: 2.4 MB (2367287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47101be2b67ca791632bd3281adfa8e5c64528b5add138395af3b54002037fa0`  
		Last Modified: Tue, 05 May 2026 23:03:20 GMT  
		Size: 18.1 KB (18064 bytes)  
		MIME: application/vnd.in-toto+json
