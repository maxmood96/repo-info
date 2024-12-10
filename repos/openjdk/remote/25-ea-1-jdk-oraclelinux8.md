## `openjdk:25-ea-1-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:1770e7f4b21be6206f904e97032448bc26ceb202ecbc0c91fe7242f4ea4246db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-1-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:593346458e354789f0c600f770f27aa108c4e248b3ad750d63b05e112fede005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279575325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaca7aa00f9750662a4052f2344c049dea59051c031d96a0823dece1b43610a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce614050030fef6add8eeab4962b8a2675627d2eee55c26e4abb2b0a2c0aeeae`  
		Last Modified: Mon, 09 Dec 2024 23:30:54 GMT  
		Size: 15.0 MB (14975187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4cf8b6048e8ab3aed24ce11e409234fe8f52d1c60a15e0458f08db9a59bdc`  
		Last Modified: Mon, 09 Dec 2024 23:30:57 GMT  
		Size: 213.3 MB (213325146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-1-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d64e01c9f2f453b65ac5be574d8d7faba57ce8071b82a4a1c9e8b1b8e46df490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613745d5465e3ce50916408723561b9e399d41dff333ce3f1c5dc01ea8c02ef9`

```dockerfile
```

-	Layers:
	-	`sha256:edceff019115a87f150b51a13f961a55fd10dcba48a95e7789f8356db062036c`  
		Last Modified: Mon, 09 Dec 2024 23:30:54 GMT  
		Size: 2.4 MB (2447748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38093a67c4daa2c9aed5c48eef82a6f9d5bdd065b99f7b119ad4f4c4cf3e1aeb`  
		Last Modified: Mon, 09 Dec 2024 23:30:54 GMT  
		Size: 16.0 KB (16020 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-1-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b221188ac1be29acab48e14fbbd1c20fa4df2cc355e9767820607d20454162b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276915435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c53160bfd53a7a4d65e85a23a9b222134dfee7f5b5c940174a098660e6cb14`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69acd795388d1f1fedcb65b1fe1cb71800f56a9beccbb0acf86fbdad421cc605`  
		Last Modified: Tue, 10 Dec 2024 01:27:38 GMT  
		Size: 15.7 MB (15659937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d027b4e8cb97911a87ca0f79d55bb64cf0c603698e38767392a122cb4188385`  
		Last Modified: Tue, 10 Dec 2024 01:27:42 GMT  
		Size: 211.3 MB (211275223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-1-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:acbfa976fe8917d46312810fb5f3a942c6b5a125aafa6e703e762591a94a6f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de732c16896f4ba46a775b263f6e72f177836933212030c9f16555e31824bf5`

```dockerfile
```

-	Layers:
	-	`sha256:c7428df73faa18ea903e0bd415f7009a945c910affe9d32983dce12efa1eeb55`  
		Last Modified: Tue, 10 Dec 2024 01:27:38 GMT  
		Size: 2.4 MB (2446592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23432254b990dd67a0dc2c7299a3dc28ed7e9c1f91e9d73a86b3569a40fb0cf5`  
		Last Modified: Tue, 10 Dec 2024 01:27:37 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json
