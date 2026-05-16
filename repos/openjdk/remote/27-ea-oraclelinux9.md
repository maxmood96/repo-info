## `openjdk:27-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:359b1c5c6d6ea9389c3ef671849d78f791ddb0c4ebfd6f61bcded7848c57e7bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:048a1d3f9fe4971f13a54b7c5cd58b08bc5ea0ad6058c6cbe3500f3302c05dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314383247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c223266c05ee2efaffb2d27462f46a05f5422717179e50ffbbd74f43211a373`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 20:18:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 May 2026 20:19:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 15 May 2026 20:19:05 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:19:05 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:19:05 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:19:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:19:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8af352b77a47154cbf02e680d0f121f17a4eef792216b9aa5714d1de770ef85`  
		Last Modified: Fri, 15 May 2026 20:19:28 GMT  
		Size: 38.3 MB (38267607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00d19fdda7297b5569156a9a07fe6c67d9b73abcb1ebd64c335bdb49e34a8a6`  
		Last Modified: Fri, 15 May 2026 20:19:31 GMT  
		Size: 228.8 MB (228806067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:b37e483097adb81f2c143dbce4beb5ebf6ff55e10964088d5f8990958a208aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ff2ed1b1083ab819d02dd0d0c9ece51887a881678e5e46368a81596addc437`

```dockerfile
```

-	Layers:
	-	`sha256:7d472385411b0fa81f05b8b23deca7f80e3d943d23209d994c1ee4ccb6febb39`  
		Last Modified: Fri, 15 May 2026 20:19:26 GMT  
		Size: 3.7 MB (3651703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:287f006ed2d151f2d2edf6e4a09052bc63850932f9354c3feea98761c26cc74e`  
		Last Modified: Fri, 15 May 2026 20:19:26 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:acb704b329f97e80f26b18669292ffc8521e605996659035a2ed62784a72b776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311325316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a5b281152c52ccdc287911a3db40b3bce03b6c67d1ee0b75d6407e740aa6ef`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 20:18:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 May 2026 20:18:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 15 May 2026 20:18:43 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:43 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:43 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:43 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02431ebd3efab545d9e7933cd33aa8fa87a3c85a02538e68b3d69903b3862b4`  
		Last Modified: Fri, 15 May 2026 20:19:06 GMT  
		Size: 38.7 MB (38663059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33491216bf17f6ddc08be92a0e0629020e23b1d20a73e1c3e2e2b8ada19d5738`  
		Last Modified: Fri, 15 May 2026 20:19:10 GMT  
		Size: 226.8 MB (226763167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:442ea6624a2a98e25a733cd13392172cc557b46250672f1f8612ac2d8f0f8989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3664759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1942825a077e48b91630eb4c062205bf75c0867f0decff902a5743c337c8156f`

```dockerfile
```

-	Layers:
	-	`sha256:90f10d011961cf801ac6273957fce4768a56bca859fb742be8d1797a1e484801`  
		Last Modified: Fri, 15 May 2026 20:19:05 GMT  
		Size: 3.6 MB (3649297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703c3c6d5e3940b0fa96ff8472a75db6e33df8d832cb56e835086e1178c97cd2`  
		Last Modified: Fri, 15 May 2026 20:19:05 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
