## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:ccd3f4730126d682cd4b0f5d0890660dc02ef80c45c9ee76a5ba13da60527838
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:756b60d182ea937f555ec9ba7c08137cdcd68bef75b0d442ccdca05668aa2766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290049731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c449607eddd5c6c7aabc3666c83e0d31a6b19e6f2a0a9525f538ac8928d6e856`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Sep 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Sep 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+14
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='14787165312e455276975549713f2f8699344989dee23e7099bafa7121b78b61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c0b7fc80b5a73fb433db4049bb05b46ed43827c082c5bfd0b6f8883400c4d91c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc03875a640d7abb05d175ce67fdabdf6304e42ecc729fec20d2f102bd8557f`  
		Last Modified: Tue, 09 Sep 2025 01:16:01 GMT  
		Size: 15.0 MB (14977138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4772251445d533d540661b14e4452c418a43f3551bb719a0eb4119e5695e1bce`  
		Last Modified: Tue, 09 Sep 2025 01:16:44 GMT  
		Size: 223.7 MB (223749030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9b9971045a91cc6db69321a2b731666e47284a0537581492a2a07dd654d9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd968bb39e0cb0df84a8c0789c086ca184c350edb2a9ebf2d1873aa49f173742`

```dockerfile
```

-	Layers:
	-	`sha256:bf0e554bfcce9650f002f376a90959f58318986446d3c78707bc9ff99448ad9c`  
		Last Modified: Tue, 09 Sep 2025 00:25:08 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c75c64c4451033d5e46ef7056d646a14683febb3103c8f240cea12b13cba549`  
		Last Modified: Tue, 09 Sep 2025 00:25:09 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:776d53b59f9a71142bf233a86d428f0d6a3fdcd6cb66cac513ec9dd7b9737c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287316532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adbbbac22e7b16f2b0902a6a82f97081a6de8051961f2e3b0797bca3ed9f762`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Sep 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Sep 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+14
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='14787165312e455276975549713f2f8699344989dee23e7099bafa7121b78b61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c0b7fc80b5a73fb433db4049bb05b46ed43827c082c5bfd0b6f8883400c4d91c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9866c68be293aa81b529074549b7f38395dba71a8ea8fc528f721fbf8543b957`  
		Last Modified: Thu, 21 Aug 2025 18:57:24 GMT  
		Size: 50.0 MB (50039817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db3d6235296211ee8b8463549ee23efff1e023085b96d1e4fd5e29796542987`  
		Last Modified: Tue, 09 Sep 2025 12:48:25 GMT  
		Size: 15.7 MB (15672283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b285945070bcf5b8b10ed8bc2379541cd40d5f98a67576d708e50da5df2872`  
		Last Modified: Tue, 09 Sep 2025 12:48:32 GMT  
		Size: 221.6 MB (221604432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b5de97dfcab4233c5ed1af215c8c2ee849b309a5ce6fcc37eb7cf27eb6a00837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4f9d396224531e9d7e6e5d906bae20dac748b0648eb5075bb2ffb3b8cebcd9`

```dockerfile
```

-	Layers:
	-	`sha256:265f9d54692cccf9d1b81a4b8338087225b0d531c40ac8f59ded88164eee7894`  
		Last Modified: Tue, 09 Sep 2025 03:24:24 GMT  
		Size: 2.4 MB (2449933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23be092de2a9b88c3981caaf6f2198e20b656917c5665ad60016ae76081bad6c`  
		Last Modified: Tue, 09 Sep 2025 03:24:25 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
