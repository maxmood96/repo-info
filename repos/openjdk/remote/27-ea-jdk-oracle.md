## `openjdk:27-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:ab4708f3ecab898d6aa895c28f7d6c2012a7bca1d3624c5ead9e1fd4fe85af91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ddf1c6bb343ea49109de9a8052fd6769ed068facabb409a93cc25a9483cb8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309561614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27947fa2d888c704c259fbc8e983232edb54fd8a8ffa5e33db8382a2367353bb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:08:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 26 May 2026 19:08:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 26 May 2026 19:08:19 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:08:19 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:08:19 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:08:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:08:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bf7577febee2eb5463e858b1308a2d14fadbbdad30d9cf809c7f0d64245e8d`  
		Last Modified: Tue, 26 May 2026 19:08:40 GMT  
		Size: 37.7 MB (37688122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329217fb40e70c44de73df02de3295e2e0fa1c6c18a8ae04d52c07f8ed6e18be`  
		Last Modified: Tue, 26 May 2026 19:08:46 GMT  
		Size: 228.8 MB (228792910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:ddc7dd8693cdf55c49489bf1661e6068495a058d9a404c0e468258d92da99d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cd246af24acb9168686beffe84490d48085b24cfbafa838be5ef667f3c80e1`

```dockerfile
```

-	Layers:
	-	`sha256:7412335a6272ef636e8caf7f68c47ef69e1ef390340fb304f87d98b92b64a271`  
		Last Modified: Tue, 26 May 2026 19:08:38 GMT  
		Size: 2.4 MB (2367747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e70f68d9566b3b1c5c2e323695f1a26c5ee00497edefdc468a0a5a52771ea5f`  
		Last Modified: Tue, 26 May 2026 19:08:38 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:782d9223d549c95bd13d999436d24bfe53c08a2db4c8d9ec36f0e727e6756fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305955314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8f9c48681fc9715930afb8c433c57b0306a34b9d6857166ea5118ac189621`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:10:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 26 May 2026 19:10:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 26 May 2026 19:10:52 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:10:52 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:10:52 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:10:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff3593a9f7badd969f2351d12f0602df5397d48593dd6e3505642689ff19df`  
		Last Modified: Tue, 26 May 2026 19:11:15 GMT  
		Size: 37.7 MB (37696071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18ed9669941852be28307f50895ca2c21b80c98a8edeec9b5f1551dec1e45f9`  
		Last Modified: Tue, 26 May 2026 19:11:18 GMT  
		Size: 226.8 MB (226763548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:93d993ac67702fcd341133722e959034585f2b9bbbc05e89422c826e72544d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1457c184c5eed6322cc524ffc08fbca8e811ca15773b92a99c6ba5e02a86a41`

```dockerfile
```

-	Layers:
	-	`sha256:f829613a2ff10657f0c31ad2c6982299e379421507299f9d7ef52e3325c13d9e`  
		Last Modified: Tue, 26 May 2026 19:11:13 GMT  
		Size: 2.4 MB (2367275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da3b16fabe506f79b39a17f3290dca105b10afcbe7f8750c1d6d9d1f9b54124`  
		Last Modified: Tue, 26 May 2026 19:11:13 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
