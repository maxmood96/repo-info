## `openjdk:27-ea-20-oraclelinux9`

```console
$ docker pull openjdk@sha256:fb99a3f505c37393e5f4bd278ce72665fbcc671ce33e513eef9c94ea80fa94da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-20-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:9e7cd6d926d92f1ec386c6c01dd229cdbe33edf5f54dea332e49eb5aeb59eb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314055248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420fa0af629faf7b1672e742acdf1d0ebcedc0b743c0a3a22c858cdea4ea4746`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:03:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:03:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 05 May 2026 23:03:24 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:03:24 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:03:24 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:03:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:03:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d6b0dcf5f560f94ac727ed2aa54fb21814f4aea693e7434da7ebbb43e23b99`  
		Last Modified: Tue, 05 May 2026 23:03:46 GMT  
		Size: 38.3 MB (38271673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378f55a21e2b6adf06b1095fd44693220d17f42ea9f002d5f9d0344d87a65de`  
		Last Modified: Tue, 05 May 2026 23:03:50 GMT  
		Size: 228.5 MB (228473719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-20-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:88509c34b4cefda82bb69ed8ab8a84c7dc3b3663dff5d901fee1e6f60268a577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe9bcfd02100ace62330e17c9461875c83dee4df3f88467d6ea71033303727`

```dockerfile
```

-	Layers:
	-	`sha256:6846847c0dde9d4dcb8bb0e7ddca55118e97ae3ab87d30d06efd437f37058dfb`  
		Last Modified: Tue, 05 May 2026 23:03:44 GMT  
		Size: 3.7 MB (3651703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ba4905bbbd3938e2e1e295a9ab62457288766843c2b4c4c773cbb245164b62`  
		Last Modified: Tue, 05 May 2026 23:03:44 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-20-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5cb5b23c3e0d2a459d75041bdb78535069def3a475778b7059680792c1e284fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310996188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e803ef52157caf492d76d780ec3a6e96a2be7042a84d6e04a42da52c76bdae7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 22:58:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 22:59:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 05 May 2026 22:59:05 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 22:59:05 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 22:59:05 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 22:59:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 22:59:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e408e430c438ab17d97763ab53ae1bd080e5cc8d53fab02dc22cd5f563f164`  
		Last Modified: Tue, 05 May 2026 22:59:27 GMT  
		Size: 38.7 MB (38662373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95b20c5e7d5b0e825077fee45b9e77fe108a8c1a54cd358a1bb50f4c50c0888`  
		Last Modified: Tue, 05 May 2026 22:59:31 GMT  
		Size: 226.4 MB (226434893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-20-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:58025d716390f13b087e2f1256d16579c806c162784a71ea400b8bce47674794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3664758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7ebf0d5ad8ae0ca2ae27407fe3c84871e88d2355853af2dca1311b3bf411f9`

```dockerfile
```

-	Layers:
	-	`sha256:6034aeaa9c24341ff32b2a4e3ce43c1531f81182547ab5f3d08ee69fb02dcdb2`  
		Last Modified: Tue, 05 May 2026 22:59:26 GMT  
		Size: 3.6 MB (3649297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62e5466b62cb2e49f5dd222c01baf9eb5d4ce7e6d8dbb0c7ff1d6ae6e8f7877e`  
		Last Modified: Tue, 05 May 2026 22:59:26 GMT  
		Size: 15.5 KB (15461 bytes)  
		MIME: application/vnd.in-toto+json
