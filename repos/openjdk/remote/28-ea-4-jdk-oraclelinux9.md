## `openjdk:28-ea-4-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:eb0d9e0653bb02647e8043334738972112726443a5d56b70f3ac5037ca64cf9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-4-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:d94fb8e440683546f5ea9664162d57385664a013fe7b0eb99729bf654dee4dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313644315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca1639098e30afdc84004d8d813e200bbd934192cebc0be1f8e5b31ced2b13`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:50:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:50:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Fri, 26 Jun 2026 17:50:13 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:50:13 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:50:13 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:50:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:50:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6b21eb7a1e3e8c85b9f7c55e523b7309abb9be51ed5d639b708a756b2568459d`  
		Last Modified: Tue, 23 Jun 2026 23:31:18 GMT  
		Size: 47.9 MB (47923466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74df5c7be8867fd9e9044b90ae0a16e12ea5cc22a56e97e21629cc05449b311`  
		Last Modified: Fri, 26 Jun 2026 17:50:36 GMT  
		Size: 38.3 MB (38301174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee32befffa0f9cee2297b1240c936b37aefa2fe89d8e88eb84c9f29683493a2`  
		Last Modified: Fri, 26 Jun 2026 17:50:40 GMT  
		Size: 227.4 MB (227419675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-4-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:a54785bfa429b8da8fd9c6588ee8bdc055449bf03367a059e853731836a4537f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ca300c3a57d33c2c1170cbf201b83c8d531270200ce628d528d930e0fc13f8`

```dockerfile
```

-	Layers:
	-	`sha256:4d6ac179dd62a203c0744e4023d0623c4de5197afeb35367b0b875b16007b052`  
		Last Modified: Fri, 26 Jun 2026 17:50:34 GMT  
		Size: 3.7 MB (3652159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee8ce32188574d48153db9564f85bdc16d4d69d0ea526609840062887acee17`  
		Last Modified: Fri, 26 Jun 2026 17:50:34 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-4-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2386dd1cba2148c06b0547608a801d460be9d4dd2920b3b85fd4bba0e9ead45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310614659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0affc4aa6889d8487782abaef028ac03b24ed57bb8d647e03924fb11eed25c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:55:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:55:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Fri, 26 Jun 2026 17:55:15 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:55:15 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:55:15 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:55:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:55:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14f0bac426a67d312501b30c0b419c0d5c2265f32077f348593b94dd76f064ac`  
		Last Modified: Tue, 23 Jun 2026 23:31:13 GMT  
		Size: 46.5 MB (46470688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396ead593db43e1989bdb7e139d36ea6b5fb3f01fb9a62accc0717a79dafabf2`  
		Last Modified: Fri, 26 Jun 2026 17:55:39 GMT  
		Size: 38.7 MB (38691373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed6e2e2879ec0097e4f4e6ad066ebdba2a2eb16c29a584d0d11a4fa4b786e1`  
		Last Modified: Fri, 26 Jun 2026 17:55:42 GMT  
		Size: 225.5 MB (225452598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-4-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:5c9d06b7ca4487f296ef3696279e12cddaac2f803d855db3d70ce0894ee38057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22df3db9ab18bc3d72bdb6406f4efd925b40c633a832cce944c1df55e22b7ce8`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd87a7fe6b0dcf0a9078b418a865fb355dd6a67916e74a9be5f52f58a2c5c9`  
		Last Modified: Fri, 26 Jun 2026 17:55:37 GMT  
		Size: 3.6 MB (3649769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03dfc6b518125631642c9cf2bd67ce7a5000cdf3387b664104730bfcbc94a0d`  
		Last Modified: Fri, 26 Jun 2026 17:55:37 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
