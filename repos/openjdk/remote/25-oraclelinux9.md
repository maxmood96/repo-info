## `openjdk:25-oraclelinux9`

```console
$ docker pull openjdk@sha256:c27d175f2a6ca5503a833dc389d85430f628d58b0c988f59b485ad7d0336769f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a5cb5d4a7921f573675d6374b574dd79154241007d8776f5928ede0b8814c03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310648292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d5d5bf5353325e38e7d4fd2e7e9e045a320ece62fbcbe1591363b9862a2455`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jul 2025 18:39:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:39:37 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad0cab3faec3438bcfbccacca666f745132fdfb9c0b58be7d741f94c36a176`  
		Last Modified: Mon, 07 Jul 2025 21:00:12 GMT  
		Size: 38.1 MB (38092469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9147bc517b3cefdb78a99efe0f50b2427dc09f0c0dc058dfd1bb7b1d57784a5d`  
		Last Modified: Mon, 07 Jul 2025 21:34:12 GMT  
		Size: 223.1 MB (223055275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:75b8173946f66cda1e6e5e0266834559e8de96d6c01c648cfcc973e15bf1b983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b888151f5447c053f82e530efa4e371b076f58c802a943b2f19ec2b35a12d7e`

```dockerfile
```

-	Layers:
	-	`sha256:cb57cc7296acb5638fdae42235171dc086cee2dec01aababa23d18ba6fd5fae1`  
		Last Modified: Mon, 07 Jul 2025 21:23:21 GMT  
		Size: 3.6 MB (3641308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a11356e5b6eff60e7136a3053b3000c501697e0448cec4a0c680469914a276f`  
		Last Modified: Mon, 07 Jul 2025 21:23:22 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f3d5b84d2f4516ebdc0664dcf6b812d835747b6b4262854e33dc4914ec1e4c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307398967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f4fa8260c06018d996985cc7ba2c23ae9abfb490bcab56fceff9628b2c80ad`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 Jun 2025 00:48:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["/bin/bash"]
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 28 Jun 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:48:09 GMT
ENV JAVA_VERSION=25-ea+29
# Sat, 28 Jun 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='4fcf990db7180589d31e39c0985acb5d19a6992d77c94892636b4035b004dd3f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/29/GPL/openjdk-25-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='565ce268822423c068fb97a832ad2c4add94427561e8e3ce29057fb8ccfbb72e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e41c14547bdbf6ff3b0e0c9c9c5853d4884135fac836a7107e73bc0a6a42f5`  
		Last Modified: Wed, 02 Jul 2025 06:14:27 GMT  
		Size: 38.5 MB (38495386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1019eb2e4d75d5d78fc3b78868d3f8afb6ef03daa894e9a0a9a428e245a198cd`  
		Last Modified: Wed, 02 Jul 2025 15:46:35 GMT  
		Size: 220.8 MB (220816497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:1c30335e67a119b3430ca3a8ae1767d76db49a110db7aab29c2a51a5d3194ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e23293189ceb8359110c63d20668ebbf720d7654f8ea15550d3add9b7e624d`

```dockerfile
```

-	Layers:
	-	`sha256:86fafb47f523c4a94898147912f3ea19e7cbb41b704bdbe1844b7407025840d7`  
		Last Modified: Wed, 02 Jul 2025 09:23:21 GMT  
		Size: 3.6 MB (3639070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30251d8cb67745cd1d9a5b8f3aaf422f2431761c4f2fd3f95c23ff1da797b2c`  
		Last Modified: Wed, 02 Jul 2025 09:23:21 GMT  
		Size: 20.0 KB (20030 bytes)  
		MIME: application/vnd.in-toto+json
