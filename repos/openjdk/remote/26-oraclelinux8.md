## `openjdk:26-oraclelinux8`

```console
$ docker pull openjdk@sha256:d0215ee4223b06cb05cd6664e8974f476e781ae0efc704274f1d57f78a52c843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0463759dd679e4ad8dd6daacb397430dc32e79dc1c91a5338c4af3838bc11a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e30af4a0c47a19cb01b17f9f452d2457971c05271ba825cea042887392ff678`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614dbc68f1a859e70aab9dace669a70347e4f90f9a37ab418478305ad68a7b61`  
		Last Modified: Tue, 02 Sep 2025 17:24:47 GMT  
		Size: 15.0 MB (14977080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc0843455956e94e9156eae567afe14d31e942df411d5aeff32b1e5df4ed657`  
		Last Modified: Tue, 02 Sep 2025 18:28:50 GMT  
		Size: 223.6 MB (223643749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:aff91952515e482358b6f812b12357adc3ee51ccb03c03416a086db6650019c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a1e78426a867125d4d6b32925fd5c2511995f0c5bca4827c464383904c3b65`

```dockerfile
```

-	Layers:
	-	`sha256:c2a490f522d25e7f3757b3f6f6766ee013a391d41cb36e806a0a8fcfe30201d5`  
		Last Modified: Tue, 02 Sep 2025 18:24:13 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f0822a3fa252d6f8e0f993657a10ed5d9fe2dc3f652e67fbdfa3470372ca72`  
		Last Modified: Tue, 02 Sep 2025 18:24:14 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a29f1fa5998fc3e8db19a0121f1403bf53faba26d90991cf2ef9ce7fb7b22f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287158455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac3a71bf08eada436912c612a55bcc14d09365c585fbcac52b1186fb09a8caa`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9866c68be293aa81b529074549b7f38395dba71a8ea8fc528f721fbf8543b957`  
		Last Modified: Thu, 21 Aug 2025 18:57:24 GMT  
		Size: 50.0 MB (50039817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a01811484fdc87c21c7358e9f38ab4c42443d4a91eff20c2aa855940ad8b39a`  
		Last Modified: Thu, 21 Aug 2025 20:17:11 GMT  
		Size: 15.7 MB (15672244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4540294c9b864535f4ff5a0212f5184345bf9161a013665f1f39322ea7f5fbc6`  
		Last Modified: Tue, 26 Aug 2025 11:47:57 GMT  
		Size: 221.4 MB (221446394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:52f6a435b254e321a15d28122a6ccdefbc9e74662571b676436679760ad72221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8878c2c2d16c7c7a562960c2928d749046b1af063e838a7f2fe38fb665e944b5`

```dockerfile
```

-	Layers:
	-	`sha256:36fed81f2660a32501c462dc2df6608ba4115523d2f1ec95b0ccb5bfa2c287d4`  
		Last Modified: Tue, 26 Aug 2025 00:24:10 GMT  
		Size: 2.4 MB (2449933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1df5006df9b23030be01544e1c204603b0ebc6b48c031396202b30a08999d7b`  
		Last Modified: Tue, 26 Aug 2025 00:24:13 GMT  
		Size: 16.2 KB (16180 bytes)  
		MIME: application/vnd.in-toto+json
