## `openjdk:25-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:210892f35af6482ef05b8409144fa1bf59588200ca7f1f4623c7017d2645a3c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:45cb451ba4e40cf623accd08dc6c335ee5dc16838f7ef02cee7e04631eb3db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310559409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01572da91492b75b0c04d71ffcda999c44017a0d1646b8027ac07afc8b3000e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:24:46 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 16:24:46 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9845df06f911da943784ccfba2249144e9c16f5ad081b3583ac643cc30b49df0`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 49.5 MB (49497893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23d8df8cc87f696bbb58f025d825b1a8c79930e21bce87f21d52e6e1ac7ed98`  
		Last Modified: Mon, 09 Jun 2025 22:07:01 GMT  
		Size: 38.1 MB (38083311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc2e6cc5b1befaf3bc3acc92011301a29a9f6d8772722d555bfbb21c3f98bfb`  
		Last Modified: Tue, 10 Jun 2025 00:48:48 GMT  
		Size: 223.0 MB (222978205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:883c9db60db0f9decf9d2e780a2cc85bf9b09d0315c89c01d070ec9acf235754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69428b8c5cdd0787412502ba77432cfa7172df5eb3122a32c61300ce56ac9908`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e80061f157736c0fb2745f5346913c17c03d011752e2c5dc975895069b4b4`  
		Last Modified: Tue, 10 Jun 2025 00:23:27 GMT  
		Size: 3.6 MB (3641236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37314215768d539e802b648a5e873218ef841e5e07f6e851e38e43691fbcbd6f`  
		Last Modified: Tue, 10 Jun 2025 00:23:27 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5fc02520792e6ef05ac16d9f5bdbd31f5852dbfbd288ec33b77b15b8b05bdd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307355571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2fb726af5b83fe7f4e356adbc82e6d8339f64dc22c4fcf995db2db27bd9c2f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:25:38 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 16:25:38 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cfd988351345b9f04447fdf8c2c46e73b5a5a2afdfe346ff0026d0c170ac82`  
		Last Modified: Tue, 03 Jun 2025 13:49:29 GMT  
		Size: 38.5 MB (38495973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b5aa78add0916ace39c3afa9cf14b69ebc9e6f691b5df9d5dfb3ed1c4c96ec`  
		Last Modified: Tue, 10 Jun 2025 01:51:22 GMT  
		Size: 220.8 MB (220769019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f6c257f44d721e62cd6214b0f04b22e438af8f06960c8e833442bee2c49bd6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9315bf9ddcb5a96017890fea7fd7a4299cfb9b4f3bf9a38264c9941a7373d520`

```dockerfile
```

-	Layers:
	-	`sha256:7926f16f05de0ae2987b10996586cb5a9efc7a9023bf37ab07ba67011feeb519`  
		Last Modified: Tue, 10 Jun 2025 00:23:32 GMT  
		Size: 3.6 MB (3638998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e28e7299dd798acd06c9e6d0206568c7715ccc1e8ebc251d8c869c1a1f7340c`  
		Last Modified: Tue, 10 Jun 2025 00:23:33 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
