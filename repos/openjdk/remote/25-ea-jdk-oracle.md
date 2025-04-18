## `openjdk:25-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:94929e447b0d654fabb12f324b49d3130648b6eb5ca62b2d2de6af668f12cc3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:0cd18107e50ce86c1c82e889c6a55596978894f99c8e1af3b2b6a6fedb736891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299569442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de5d7640f0603d21336ecfa6efbac258fd8fbac44c6e045cfdbac2f7b7d3c05`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 31 Mar 2025 23:38:24 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:38:24 GMT
CMD ["/bin/bash"]
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ce76d58ea1f27cda7f7fb3fd5160b05eef2c2a89d0f9259d5e864dd5ec9985`  
		Last Modified: Fri, 18 Apr 2025 18:37:58 GMT  
		Size: 38.1 MB (38105996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d74916db3b49c7d9b4c4c67fa8026ede811ec25ee41adcb684c34dbe9a51851`  
		Last Modified: Fri, 18 Apr 2025 18:38:00 GMT  
		Size: 212.4 MB (212372236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:70ced6508e9f6b164ea216113a84e1f5891d708a3d048fffd03ec1484b1903ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3644252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33b1ec9ea9d5c90a9a8c8d8211539b5a24adf3706b6441fe1447027fe471349`

```dockerfile
```

-	Layers:
	-	`sha256:92d5626e06aeb22901d6dd41590e760e1630d174328345cf46e72800d90689e1`  
		Last Modified: Fri, 18 Apr 2025 18:37:57 GMT  
		Size: 3.6 MB (3624506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8f757dd883a2c8e17a564c7ab3716f7a1b313107603d807dabfa7f1279f4f1`  
		Last Modified: Fri, 18 Apr 2025 18:37:57 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:93221791d8db8a30ab6156608483e93806137a961ad920717a45d346744c1831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296372987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba08fde822f31506ad7890d3994c0b643e994e1f33439661c2816877ec3f24af`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 31 Mar 2025 23:39:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 31 Mar 2025 23:39:16 GMT
CMD ["/bin/bash"]
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5750f1793fdd6894b80fd32af7c3dc7fd61fe28a4003df2c3b5206dfd9ecf575`  
		Last Modified: Mon, 14 Apr 2025 22:58:29 GMT  
		Size: 38.5 MB (38500787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7e910b01b482a5247db8bfea49151fd73086d3c3fa066ed7be33722b1ecef5`  
		Last Modified: Fri, 18 Apr 2025 18:37:37 GMT  
		Size: 210.2 MB (210197377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:618225cd03ead93ba147ffb4dabc1e4cca18f8b2e6b8828c379415a18dd18938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709269643d6d36353c04b12d3319fa7fc4aa46ef96c311e9361fb19c1d727fcc`

```dockerfile
```

-	Layers:
	-	`sha256:ea3ba60ecbf0780478ab59d03a446f1fec978fe6267e8031170af4c7396e6440`  
		Last Modified: Fri, 18 Apr 2025 18:37:33 GMT  
		Size: 3.6 MB (3622268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d61c727550986f40dd9b8037974f68fb1c9041004fa50c4e6d5c0fa6ee2fca`  
		Last Modified: Fri, 18 Apr 2025 18:37:32 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
