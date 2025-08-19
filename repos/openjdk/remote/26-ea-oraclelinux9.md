## `openjdk:26-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:ad6f18af3a01c81aafe145e94f4dbe682ed98c1791820815be4701ea38f4b388
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a1720248aec330b3ead83f60b4dc28c53a7d74bbcf9246e7ec561626ce9c3a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310528768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce0330aec9e7407ebbb9359b2634d8d96aa99aa54445880792cc62dee2248c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:10aec8a104c7ecf055b7137fb34a3666fce4dff1b9f6d210fb88eaddd4c8c329`  
		Last Modified: Thu, 07 Aug 2025 23:49:00 GMT  
		Size: 49.5 MB (49497127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f567055f5f40f58dca680b7e795db9b1b2a2c11b941ba7f468f50ed933a109c`  
		Last Modified: Mon, 18 Aug 2025 18:16:52 GMT  
		Size: 38.0 MB (38006630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e94c6bab18dd0bc295313e435838503869082a0366afb4cbedd56042ef68ed`  
		Last Modified: Mon, 18 Aug 2025 21:30:31 GMT  
		Size: 223.0 MB (223025011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:ecd5da9a8533dda614bd1aab2f0d05d058a4f95028f6d45d76094c16dd925b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7f55074832934c93d8c509ef3cb35f042522279c7e2bc4b9cdb571d4225d32`

```dockerfile
```

-	Layers:
	-	`sha256:460a27ca7d67d8f482e0076af174f89442834ed4f869b058e869085ca7e0acf3`  
		Last Modified: Mon, 18 Aug 2025 21:24:51 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a8f57fe844299865d851f3cfb02b07ee47b9627f1ab4b1fb349a509e6365d19`  
		Last Modified: Mon, 18 Aug 2025 21:24:52 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3e3792bd10b348c336f0a1a91df24ba4d9aed995f6346cf36bb68b2e990353ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307364405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6687cb03b3dcc707794a20ba3ced51cd1ab14a844dd9db3744f196bd27d791`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c27940f400cbdef01d301fb84d1331162f6c76466797e235ea774e439f357`  
		Last Modified: Mon, 18 Aug 2025 22:21:13 GMT  
		Size: 38.4 MB (38409969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830f967eb116cda4aa6f90002fdb92ccad3c952b995f0c3f89b87f31e327e7fc`  
		Last Modified: Tue, 19 Aug 2025 03:02:01 GMT  
		Size: 220.9 MB (220867525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:1b0ca0042b9667987afb8ba7f5c7267ee7e6345f2d8c90d1b248ca43f5e8173d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9182eb92201414f3ef4d2a6a44087bca4917460a27c610757c044bd8dcfcc92`

```dockerfile
```

-	Layers:
	-	`sha256:ec8b7a7f762c19f0871d2b75d3ff8b4987ff6ca633227bf6acbbceed7659f163`  
		Last Modified: Tue, 19 Aug 2025 00:24:31 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c3c692a419632436b1e2e3f8d5d8c12ef795e554d815536cf6317a91dba919d`  
		Last Modified: Tue, 19 Aug 2025 00:24:32 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.in-toto+json
