## `openjdk:27-ea-27-oraclelinux9`

```console
$ docker pull openjdk@sha256:64b6c76754d578e7aed9676c9d8ec136935bd069b16be62e3bd768af80b387c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-27-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:131238c9e61721cc5312ba16605d89e3c30edfc0c64c688e6961332ec264c8df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313909900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d288f1273bbb9eea8d9fe8afa5bf9527d03bcd598c28ba3d25ee833f144dd1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:38:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:38:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 22 Jun 2026 22:38:21 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:21 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:21 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:38:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876e38ad252f678a7f8493fd6ed1a47d36663245c009df429024d6e79d7a5e64`  
		Last Modified: Mon, 22 Jun 2026 22:38:45 GMT  
		Size: 39.7 MB (39652399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7939d83855d5fe7bc73d66766101d071ea6b7f3feb3f171b86839fa52dab41b9`  
		Last Modified: Mon, 22 Jun 2026 22:38:48 GMT  
		Size: 226.9 MB (226947928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:437551f5cbdd07a11e028d73952099218e6c85d4d0d9832128123d450792306f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c9b340db3357ed112146daf985db33041f72d967d6a4661da88f9bad963ea1`

```dockerfile
```

-	Layers:
	-	`sha256:c27d20c10e7f16290f5711eb672403d8fb398176dcaeab68526b2facb287df6e`  
		Last Modified: Mon, 22 Jun 2026 22:38:43 GMT  
		Size: 3.7 MB (3676554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae149147889e4213a503866e87a08e0988afd85f46038b52749c497ac418125a`  
		Last Modified: Mon, 22 Jun 2026 22:38:43 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-27-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9a90a0da56c77d88b00b9474b7c3b715919675d0a620e3ce30db683e9e8c7246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310880227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964af5e1282c8f2a18e9d5dd09b97dab2945a3c2392bf03b5bde2191f7edde99`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:37:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:38:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 22 Jun 2026 22:38:06 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:06 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:06 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:38:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359b72e6c1a2bd6351b1d4d524c15c70a818ae4aa928b58c9895d4d774b095fd`  
		Last Modified: Mon, 22 Jun 2026 22:38:30 GMT  
		Size: 40.0 MB (40046930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a20eb15222561e172b1b3088fc94ea1af24c18a69cd70ae5783fae9dbf08728`  
		Last Modified: Mon, 22 Jun 2026 22:38:34 GMT  
		Size: 224.9 MB (224934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:0c5bc0738c0efc6e22be7ed81dafb21311f673f253c88acab47dfa3024543046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e43fdf18f2856fbd19347984860faa11ee51c88301b17e9f8c0e16e6e203bb`

```dockerfile
```

-	Layers:
	-	`sha256:6d9b2c746af1447d6f166e1d813e1d8d5c6191ec8d3117b5371e41bcc09ffcd3`  
		Last Modified: Mon, 22 Jun 2026 22:38:28 GMT  
		Size: 3.7 MB (3674148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd6083d4b88911bfe0145f470b1a601095874c99f9434863bdad49e04c900d8`  
		Last Modified: Mon, 22 Jun 2026 22:38:28 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
