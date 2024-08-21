## `openjdk:24-ea-11-oracle`

```console
$ docker pull openjdk@sha256:cf92e7a2dcb16a1a4b9105d68920061b96255f2ee9f1ea7bdfe21a7bcd4d8179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-11-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:f3b69cb3fa172881d2ea9f0e4788527d6ea6bf1c45c8ca66e16af0a6b96c528c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299798285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03a7361f764af255d8281fe056724929bfc3b71cdf890674c887a454f76c041`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["/bin/bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51423d70752a8af6f46da49d1118e48f7eacad87fa460cea855c86e7abe5150`  
		Last Modified: Wed, 21 Aug 2024 01:06:28 GMT  
		Size: 39.0 MB (39046709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bc51f9c1a3ee526f4045af4c37ddd049cb6734fd1c7919275492b85c0c849`  
		Last Modified: Wed, 21 Aug 2024 01:06:31 GMT  
		Size: 211.8 MB (211756755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-11-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:2a467feeae15383bac92b89d0b3807e5cfd21c146774a97eb19656690233e468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e538fccda0031b07627ea9583c3f80abb9e304aab07916cb1253f2e1138da`

```dockerfile
```

-	Layers:
	-	`sha256:0a2aa2ba8bc82097a860a64a80af3017ccd57ccf40bc74baeb29a0eab830e1e4`  
		Last Modified: Wed, 21 Aug 2024 01:06:27 GMT  
		Size: 3.5 MB (3545985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d44fe02863cbfb265ccf653f79716fc0f625dd89f566a1a5dd8862041232fa8`  
		Last Modified: Wed, 21 Aug 2024 01:06:27 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-11-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a235be72d2da585c19de02e23d39608ade2c6dc3508d6b703db18138194c6dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296741247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28486793e9c481b73b573b4564b1e5064fed9e5c5daaeefaddb5028b8b8e396`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["/bin/bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64a371a7ad1ff13a4dded4febe3bd91f6ddf3dac8b18dc7feef6e025c2943f3`  
		Last Modified: Wed, 21 Aug 2024 01:11:51 GMT  
		Size: 39.5 MB (39478981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d843b766bf93c7faa6e0eb014ff3ba6dc299de0fefa821aa723ac47ac4c591`  
		Last Modified: Wed, 21 Aug 2024 01:11:55 GMT  
		Size: 209.6 MB (209607700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-11-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b554ec1cce800f3afc56954d457e95bf63195e70aee184401f21f0a82afac1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60842824e85ebcf9160738ba2e3c3790341d60783907da99434bc403fae77a30`

```dockerfile
```

-	Layers:
	-	`sha256:edc1f213df313cdb112646ef05aba2f536f683d138fca0acca5bcead2b803582`  
		Last Modified: Wed, 21 Aug 2024 01:11:50 GMT  
		Size: 3.5 MB (3544368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a767213f1986303c48f27f4f2587b687bb09c945c13625a231e65083fe746ab9`  
		Last Modified: Wed, 21 Aug 2024 01:11:50 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json
