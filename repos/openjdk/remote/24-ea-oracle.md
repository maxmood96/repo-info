## `openjdk:24-ea-oracle`

```console
$ docker pull openjdk@sha256:e7259cfac259d4af142dfdeed68f3d162276b9619d6f8377a8d646312b649b5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:83859658291382b42d6604876da3f69a53d3d5070a8af19783d684419499b1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300559178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71906a9a4cb55f8aa956784ba4f6b0f2721508ba48721687ef0844af6d72a43`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372fe839ed39262adbb1f6d23c1af7c162bcd3754ad18177c82a431fdbdaf258`  
		Last Modified: Fri, 11 Oct 2024 18:57:58 GMT  
		Size: 39.1 MB (39059300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448d8ad0d2daa34c775577b96d9acc4e720b0a558910d9b693f7c00eb47c0c32`  
		Last Modified: Fri, 11 Oct 2024 18:58:01 GMT  
		Size: 212.3 MB (212252936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:3a44264e5e1005852495f4fade72b42986e2c2e06414626260e01e5b12bf38e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ea67ca7449c0edccf92654bb09e611b47921f5ad710afd39136b552005c770`

```dockerfile
```

-	Layers:
	-	`sha256:1a7038dc230cef74c27005b3d4863f709f0b1e928a278071dac4e7e6f454c274`  
		Last Modified: Fri, 11 Oct 2024 18:57:57 GMT  
		Size: 3.8 MB (3782218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026399dc38e2686b740925a8d524ca06f90809712c76838da6d49320a3700813`  
		Last Modified: Fri, 11 Oct 2024 18:57:58 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:086ddcba6a252188c529e20a92cd1530f5de70fc3094bde10b0255bee08c15c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297540087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877477fbc5dcef2765a5d577ed19b9867e3ff7e47c624415689f0d0bdff75607`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4830f0617e169814cdd037593b108be4e44c65fea0cd14bea2f550048d73af5`  
		Last Modified: Fri, 11 Oct 2024 19:23:54 GMT  
		Size: 39.5 MB (39490897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140db9f79b214672480b78ff6ff1f6f4c5937855bbfe928bb083284e56c98224`  
		Last Modified: Fri, 11 Oct 2024 19:23:57 GMT  
		Size: 210.1 MB (210134607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d1d9c5477966667869e1f94684d4b1ef0f6512fdaab18b1d0068b7a4d2c0eb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1f6495ba47451ca991ba162af84fb6a889feca5210ad721fce3332a695f6b9`

```dockerfile
```

-	Layers:
	-	`sha256:53833d2413a276db5d9a85668aa21726e64b05378670edffebf6c50a64eaaaef`  
		Last Modified: Fri, 11 Oct 2024 19:23:53 GMT  
		Size: 3.8 MB (3779354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda69cfaf38c45a4f5b8c7e00115208c9a3397e06b2ad0109f9f44a667ec2b69`  
		Last Modified: Fri, 11 Oct 2024 19:23:52 GMT  
		Size: 20.0 KB (20037 bytes)  
		MIME: application/vnd.in-toto+json
